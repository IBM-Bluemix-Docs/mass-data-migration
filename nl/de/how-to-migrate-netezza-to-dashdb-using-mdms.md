---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-31"

---
{:codeblock: .codeblock}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Netezza-Datenbanken auf DashDB migrieren

Mit dem Mass Data Migration Service (MDMS) können umfangreiche Netezza-Datenbanken auf DashDB migriert werden. Sie können dieses Dokument als Referenz für die Tools verwenden, mit denen die Menge der zu übertragenden Daten und die Exportmethoden festgelegt werden.

## Größe des Datenbankobjekts ermitteln
1. Laden Sie von [IBM Support > Fix Central > Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window} die geeignete Version der Netezza-Tools für Ihre Netezza-Instanz herunter.

   Unterstützungstools werden auf dem Netezza-Server standardmäßig im Verzeichnis `/nz/support-IBM_Netezza<version>/bin` installiert.
   {:note}

2. Führen Sie die beiden folgenden Befehle aus.
   - `nz_db_size`, um die Größe der Datenbank zu bestimmen.

     ```
     nz_db_size
     Objekt | Name | Byte  | KB | MB | GB | TB
     -----------------------------------------------------------------------------------------------------------
     Appliance | cdcntze1 | 23.388.712.337.408 | 22.840.539.392 | 22.305.214 | 21.782,4 | 21,3
     Datenbank | DHDB | 183.537.500.160 | 179.235.840 | 175.035 | 170,9 | 0,2
     Tabelle | DH71964I1 | 880.803.840 | 860.160 | 840 | 0,8 | 0,0
     Tabelle | DH71964T1 | 96.120.078.336 | 93.867.264 | 91.667 | 89,5 | 0,1
     Tabelle | DH71964T10 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T2 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T3 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T4 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T5 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T6 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T7 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T8 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     Tabelle | DH71964T9 | 9.615.179.776 | 9.389.824 | 9.170 | 9,0 | 0,0
     ```
     {: codeblock}

   - `nz_compressedTableRatio`, um die Größe der dekomprimierten Daten zu schätzen.

      ```
      nz_compressedTableRatio
  ....................................................................................
      . Die Werte zeigen das geschätzte Größenverhältnis einer komprimierten Tabelle .
      . zu der entsprechenden nicht komprimierten Tabelle. Eine nicht komprimierte .
. Tabelle ist ungefähr <ratio> mal größer als die entsprechende
      . . nicht komprimierte Tabelle. .
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
      {: codeblock}

## Daten extrahieren und Onboarding

Sie können zwei Optionen verwenden, um die Daten aus Netezza zu extrahieren.
- Verwenden Sie das Dienstprogramm `nz_backup`.
   ```
   /nz/support/contrib/bin/nz_backup –db   {DB-Name} –d  {Zielverzeichnis}  ascii threads 4
   ```

   Das `{Zielverzeichnis}` ist die gemeinsam genutzte NFS-Ressource, die von der MDMS-Einheit bereitgestellt wird und die auf diesem Server angehängt ist.
   {:tip}

- Verwenden Sie die Anweisung `CREATE EXTERNAL TABLE`.
   - Wählen Sie `FORMAT` = ”Text” aus.
   - Stellen Sie dem DashDB-Team die `USING`-Klausel zur Verfügung, die beim `LOAD`-Prozess für den Export für die Wiederverwendung verwendet wurde.


## Daten überprüfen
Die Daten können wieder in Netezza eingelesen werden, um sicherzustellen, dass sie korrekt sind. Verwenden Sie dazu die Anweisung `SELECT FROM` mit der externen Tabelle `myfile` und einer `USING(....)`-Klausel.

**Weitere Informationen**

Weitere Informationen zu Netezza sind in der [Benutzerdokumentation zur IBM Netezza-Datenbank](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window} verfügbar.
