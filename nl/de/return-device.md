---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# Einheit zurückgeben
{: #return-device}

Schalten Sie Ihre {{site.data.keyword.mdms_full}}-Einheit aus und geben Sie sie an {{site.data.keyword.cloud_notm}} zurück, um den Migrationsprozess abzuschließen.
{: shortdesc}

## Kabelverbindungen der Einheit trennen
{: #disconnect-device}

Wenn der Datenkopierprozess abgeschlossen ist, können Sie das System ordnungsgemäß ausschalten. 

1. Klicken Sie im Assistenten für allgemeine Tasks auf **Appliance beenden**. 

    ![Appliance beenden](images/ShutDown.png)

Klicken Sie zur Bestätigung auf **OK**. 2. Schalten Sie die Einheit über die Taste **System ein/aus** an der Einheit aus.  
3. Bringen Sie den **Hauptschalter** in die Position **Aus**. 
4. Wickeln Sie die Kabel auf und legen Sie alle Kabel und optischen Kabel in die jeweiligen Aufbewahrungstaschen im Transportbehälter. 

## Einheit an {{site.data.keyword.cloud_notm}} senden
{: #ship-device}

Bereiten Sie die Versandaufkleber vor und benachrichtigen Sie das Versandunternehmen, wenn die Einheit für die Rücksendung bereit ist. 

1. Entnehmen Sie die Bestandsliste und den Rücksendeaufkleber für die Einheit. Diese Dokumente befinden sich unter der Abdeckung des Transportbehälters. 

Wenn Sie mehrere Geräte versenden, müssen Sie beachten, dass der jeweils bereitgestellte Rücksendeaufkleber für die Speichereinheit spezifisch ist. Bevor Sie einen Abholtermin mit dem Versandunternehmen vereinbaren, stellen Sie sicher, dass auf jeder Einheit der korrekte Rücksendeaufkleber angebracht wurde.
    {: note}
2. Überprüfen Sie anhand der Bestandsliste, ob alle Kabel und optischen Module sich im Transportbehälter befinden, sodass sie zurückgegeben werden. 
3. Legen Sie die Bestandsliste wieder in den Transportbehälter und befolgen Sie anschließend die Anweisungen auf dem Rücksendeaufkleber, um den Aufkleber an der Einheit anzubringen. 
4. Vereinbaren Sie einen Abholtermin mit dem Versandunternehmen und senden Sie die Einheit an das Rechenzentrum zurück. 

    Wenn die Einheit an {{site.data.keyword.cloud_notm}} zurückgegeben wird, ändert sich der Status der Bestellung auf der {{site.data.keyword.mdms_short}}-Anforderungsdetailseite in _Einheit erhalten_. 

## Nächste Schritte
{: #return-device-next-steps}

- Überprüfen Sie den Status Ihrer Bestellung wie in [{{site.data.keyword.mdms_short}}-Anforderung verwalten](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request) beschrieben. 
- Bevor Sie Daten auf Ihrem Quellenserver löschen, [überprüfen Sie, ob die Daten erfolgreich in {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data) hochgeladen wurden. 

