---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# Speicherpool entsperren
{: #unlock-storage-pool}

Bevor Sie Daten auf die {{site.data.keyword.mdms_full}}-Einheit kopieren können, müssen Sie zuerst den Speicherpool entsperren und aktivieren, der für die Einheit bereitgestellt wird.
{: shortdesc}

## Kennphrase für Speicherpool abrufen (Betaversion)
{: #retrieve-storage-pool-passcode}

Zum Zugreifen auf den Speicherpool auf der {{site.data.keyword.mdms_short}}-Einheit rufen Sie Ihre Einheitenberechtigungsnachweise ab, indem Sie in der {{site.data.keyword.cloud_notm}}-Konsole zu den {{site.data.keyword.mdms_short}}-Anforderungsdetails navigieren. 

Dieses Feature ist als Bestandteil der [Betaversion von {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta) verfügbar. Sie können auch über den Abschnitt _Anforderungsdetails_ im [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} auf die Berechtigungsnachweise für Ihre Speichereinheit zugreifen.
{: note}

Gehen Sie wie folgt vor, um die Kennphrase Ihres Speicherpools abzurufen: 

1. [Melden Sie sich bei der {{site.data.keyword.cloud_notm}}-Konsole an](https://{DomainName}/){: external}. 
2. Rufen Sie **Menü** &gt; **Ressourcenliste** auf, um eine Liste Ihrer Ressourcen anzuzeigen. 
3. Wählen Sie in Ihrer {{site.data.keyword.cloud_notm}}-Ressourcenliste Ihre bereitgestellte {{site.data.keyword.mdms_short}}-Instanz aus. 
4. In der Registerkarte _Anforderungsdetails_ navigieren Sie zum Abschnitt 'Berechtigungsnachweise'. 
5. Kopieren Sie den Wert für **Kenncode für Poolsperre**. 

## Speicherpool aktivieren
{: #activate-storage-pool}

Entsperren Sie den leeren Speicherpool mithilfe der Berechtigungsnachweise, die Sie im vorherigen Schritt abgerufen haben. 

1. [Melden Sie sich bei der Benutzerschnittstelle der Einheit an](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui). 
2. Klicken Sie im Assistenten für allgemeine Tasks auf **Speicherpool entsperren und starten**. 
3. Geben Sie die Kennphrase für den Speicherpool ein, die Sie in Schritt 1 abgerufen haben, und klicken Sie anschließend auf **OK**. 
      
   ![Speicherpool aktivieren](/images/StartStoragePool.png)

   Standardmäßig sind für die gemeinsam genutzte Ressource sowohl das NFS-Protokoll (Network File System) als auch das SMB-Protokoll (Server Message Block) ohne Zugriffsbeschränkungen aktiviert. Sie können den Zugriff auf diese gemeinsam genutzte Ressource für NFS oder SMB ändern, indem Sie in der Benutzerschnittstelle mit der rechten Maustaste auf den Namen der Ressource klicken und dann die entsprechende Menüoption auswählen.
   {: note}

## Nächste Schritte
{: #unlock-storage-pool-next-steps}

- Wenn Sie eine UNIX-Maschine verwenden, [stellen Sie über NFS eine Verbindung zu dem gemeinsam genutzten Netzbereich her](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share). 
- Wenn Sie eine Windows-Maschine verwenden, [stellen Sie über SMB eine Verbindung zu dem gemeinsam genutzten Netzbereich her](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share). 
- Starten Sie den [Datenkopierprozess](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy). 
