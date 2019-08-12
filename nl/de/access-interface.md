---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# Auf die Benutzerschnittstelle der Einheit zugreifen
{: #access-ui}

Nach der Konfiguration der {{site.data.keyword.mdms_full}}-Einheit für Ethernet-Konnektivität sind Sie für den Zugriff auf die Benutzerschnittstelle der Einheit bereit, sodass Sie mit der Einheit interagieren und den Datenmigrationsprozess starten können.
{: shortdesc}

## Einheitenberechtigungsnachweise abrufen (Betaversion)
{: #retrieve-device-credentials}

Wenn Sie eine {{site.data.keyword.mdms_short}}-Anforderung übergeben, generiert der Service automatisch Berechtigungsnachweise in Ihrem Namen. Diese können Sie für den Zugriff auf die lokale Webbenutzerschnittstelle für die Einheit verwenden.  

Dieses Feature ist als Bestandteil der [Betaversion von {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta) verfügbar. Sie können auch über den Abschnitt _Anforderungsdetails_ im [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} auf die Berechtigungsnachweise für Ihre Speichereinheit zugreifen.
{: note}

Gehen Sie wie folgt vor, um die Berechtigungsnachweise für Ihre Einheit abzurufen: 

1. [Melden Sie sich bei der {{site.data.keyword.cloud_notm}}-Konsole an](https://{DomainName}/){: external}. 
2. Rufen Sie **Menü** &gt; **Ressourcenliste** auf, um eine Liste Ihrer Ressourcen anzuzeigen. 
3. Wählen Sie in Ihrer {{site.data.keyword.cloud_notm}}-Ressourcenliste Ihre bereitgestellte {{site.data.keyword.mdms_short}}-Instanz aus. 
4. In der Registerkarte _Anforderungsdetails_ navigieren Sie zum Abschnitt 'Berechtigungsnachweise'. 
5. Kopieren Sie die Werte für **Benutzername** und **Kennwort**. 

## Bei der Benutzerschnittstelle der Einheit anmelden
{: #log-in-ui}

Verwenden Sie die im vorherigen Schritt abgerufenen Einheitenberechtigungsnachweise, um sich bei der lokalen Webbenutzerschnittstelle anzumelden und mit der {{site.data.keyword.mdms_short}}-Einheit zu interagieren. 

1. Öffnen Sie einen Webbrowser und navigieren Sie zu der statischen IP-Adresse, die Sie im Bestellformular angegeben haben. 

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Ersetzen Sie `<device_management_IP_address>` durch die IP-Adresse, die für Ihren Netzport 'Eth1' oder 'Eth2' konfiguriert ist. Akzeptieren Sie die angezeigte Zertifikatsausnahme.

2. Melden Sie sich bei der Benutzerschnittstelle der Einheit mit dem Benutzernamen und dem Kennwort an, die Sie im vorherigen Schritt abgerufen haben.  

   ![Anmeldeseite](images/login.png)
   
   Der Assistent für allgemeine Tasks wird angezeigt. Verwenden Sie die Optionen von links nach rechts, um mit dem Import Ihrer Daten zu beginnen. 

   ![Workflowsymbole](images/workflow.png)

   Sie können den Assistenten für allgemeine Tasks erneut öffnen, indem Sie den **Workflow-Manager** im oberen linken Bereich der Schnittstelle verwenden.
   {:tip}

## Nächste Schritte
{: #access-ui-next-steps}

- Beginnen Sie mit der [Entsperrung des Speicherpools auf der Einheit](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool), um den Kopierprozess für die Datenaufnahme vorzubereiten. 
