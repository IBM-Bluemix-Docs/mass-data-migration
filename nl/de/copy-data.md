---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: copy data to device, move data to device, 

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Daten auf die Einheit kopieren
{: #copy-data}

Sie können Daten mithilfe der Benutzerschnittstelle der Einheit auf eine {{site.data.keyword.mdms_full}}-Einheit kopieren. 

## Daten auf die Einheit kopieren
{: #copy-data}

Nachdem Sie Ihren Server mit dem gemeinsam genutzten Netzbereich verbunden haben, können Sie die Datenkopie auf die Einheit starten und überwachen. 

1. Verwenden Sie ein Dateikopiertool, das mit Ihrem Host-Computer kompatibel ist, um Daten auf den gemeinsam genutzten Netzbereich zu kopieren. 
2. Klicken Sie im Assistenten für allgemeine Tasks auf **Netzaktivität anzeigen**, um die eingehende Ethernet-Last anzuzeigen, während Daten über die 10-Gb-Verbindung auf die Einheit übertragen werden. 
   
    ![Aktivität anzeigen](images/NetworkPerf.png)
3. Klicken Sie auf **Speicherpool anzeigen**, um die Speicherbelegung und die E/A-Operationen pro Sekunde auf der Einheit zu überwachen. 
   
    ![Speicherpool anzeigen](images/PoolPerf.png)

## Nächste Schritte
{: #import-data-next-steps}

- [Schalten Sie die Einheit ordnungsgemäß aus](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device). 
- Bereiten Sie den Versandaufkleber vor und [senden Sie die Einheit an {{site.data.keyword.cloud_notm}} zurück](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device). 
