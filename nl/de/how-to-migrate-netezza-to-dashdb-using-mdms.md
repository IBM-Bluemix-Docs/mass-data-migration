---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Netezza-Datenbanken auf DashDB migrieren

Mit dem Service für Massendatenmigration (Mass Data Migration Service, MDMS) können umfangreiche Netezza-Datenbanken auf DashDB migriert werden.

In diesem Dokument wird Folgendes beschrieben:
- Netezza-Tools zum Ermitteln des Datenvolumens, das mit dem Service für Massendatenmigration übertragen werden soll
- Befehle zum Exportieren der Daten in die Einheit für Massendatenmigration

## Datenbankdimensionierung
1. Laden Sie die geeignete Version der Netezza-Tools für Ihre Netezza-Instanz von [IBM Support: Fix Central - Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window} herunter.

   **Hinweis**: Unterstützungstools werden auf dem Netezza-Server standardmäßig im Verzeichnis /nz/support-IBM_Netezza<version>/bin installiert.
   
2. Die beiden folgenden Befehle können verwendet werden: `nz_db_size` und `nz_compressedTableRatio`

```
nz_db_size
Objekt | Name | Byte | KB | MB | GB | TB
-----------------------------------------------------------------------------------------------------------
Appliance | cdcntze1 | 23.388.712.337.408 | 22.840.539.392 | 22.305.214 | 21.782,4 | 21,3
Datenbank | DHDB | 183.537.500.160 | 179.235.840 | 175.035 | 170,9 | ,2
Tabelle | DH71964I1 | 880.803.840 | 860.160 | 840 | ,8 | ,0
Tabelle | DH71964T1 | 96.120.078.336 | 93.867.264 | 91.667 | 89,5 | ,1
Tabelle | DH71964T10 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T2 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T3 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T4 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T5 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T6 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T7 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T8 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
Tabelle | DH71964T9 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | ,0
```
```
nz_compressedTableRatio
....................................................................................
. Die Werte zeigen das geschätzte Größenverhältnis einer komprimierten Tabelle .
. zu der entsprechenden nicht komprimierten Tabelle. Eine nicht komprimierte .
. Tabelle ist ungefähr <ratio> mal größer als die entsprechende . 
. nicht komprimierte Tabelle. .
. .
. Die 'Komprimierte Größe' gibt an, wie viel Speicher die Tabelle belegt. .
. Die 'Unkomprimierte Größe' ist ein mathematisch berechneter Schätzwert. .
....................................................................................
Datenbank: DHDB
Tabelle/MView-Name Ratio Komprimierte Größe Unkomprimierte Größe Größendifferenz
================== ===== ================ =============== ===========
DH71964I1 1,49 880.803.840 1.310.723.840 429.920.000
DH71964T1 1,50 96.120.078.336 144.179.203.840 48.059.125.504
DH71964T10 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T2 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T3 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T4 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T5 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T6 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T7 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T8 1,50 9.615.179.776 14.417.923.840 4.802.744.064
DH71964T9 1,50 9.615.179.776 14.417.923.840 4.802.744.064
================================ ===== =================== ===================
Summe für diese Datenbank 1,50 183.537.500.160 275.251.242.240 91.713.742.080
```

## Prozedur für Datenextraktion und Onboarding

Zum Extrahieren der Daten aus Netezza stehen zwei Optionen zur Verfügung:
1. Verwendung des **Dienstprogramms 'nz_backup'**:

   `/nz/support/contrib/bin/nz_backup –db   {db-name} –d  {zielverzeichnis}  ascii threads 4`
   
   **Hinweis**: Das {zielverzeichnis} ist die vom MDMS-Gerät bereitgestellte, gemeinsam genutzte NFS-Ressource, die an diesen Server angehängt ist.
2. Erstellen einer externen Tabelle (CREATE EXTERNAL TABLE)
   - Stellen Sie dem DashDB-Team die Klausel “USING” zur Verfügung, die beim LOAD-Prozess zum Exportieren für die Wiederverwendung verwendet wird.
   - Wählen Sie FORMAT = ”Text” aus.
   
   
## Datenvalidierung
Die Daten können unter Verwendung von 'select from external table **meinedatei** `USING(....) “`' erneut in Netezza gelesen werden, um sicherzustellen, dass die Daten korrekt sind.
 
## Zusätzliche Informationen
Weitere Informationen zu Netezza finden Sie in der [Dokumentation für IBM Netezza-Datenbankbenutzer](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
