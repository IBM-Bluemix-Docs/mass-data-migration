---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# Daten überprüfen
{: #verify-data}

Mit {{site.data.keyword.cos_full}} können Sie auf Ihre migrierten Daten zugreifen und diese überprüfen.
{: shortdesc}

Wenn die Auslagerung abgeschlossen ist, können Sie sofort auf Ihre Daten in der Cloud zugreifen, während {{site.data.keyword.cloud_notm}} die Einheit sicher bereinigt. 

## Auf Ihre Daten in Cloud Object Storage zugreifen
{: #access-data-cos}

Ihre migrierten Daten sind in der Cloud Object Storage-Instanz verfügbar, die Sie bei der Übergabe Ihrer {{site.data.keyword.mdms_short}}-Anforderung angegeben haben. Überprüfen Sie, ob die Daten erfolgreich in {{site.data.keyword.cloud_notm}} hochgeladen wurden, bevor Sie Daten auf Ihrem Quellenserver löschen. 

Gehen Sie wie folgt vor, um auf Ihre Daten zuzugreifen und sie zu überprüfen:  

1. [Melden Sie sich bei der {{site.data.keyword.cloud_notm}}-Konsole an](https://{DomainName}/){: external}. 
2. Rufen Sie **Menü** &gt; **Ressourcenliste** auf, um eine Liste Ihrer Ressourcen anzuzeigen. 
3. Wählen Sie in Ihrer {{site.data.keyword.cloud_notm}}-Ressourcenliste Ihre bereitgestellte Instanz von Cloud Object Storage aus. 
4. Wählen Sie in der Liste der verfügbaren Speicherbuckets den Bucketnamen aus, den Sie für die Datenmigration angegeben haben. 
5. Prüfen Sie, ob die dem Bucket zugeordneten Objekte den Daten entsprechen, die Sie auf die {{site.data.keyword.mdms_short}}-Einheit kopiert haben. 

## Daten in eine andere Speicherlösung verschieben
{: #move-data}

Je nach Ihren Workloadanforderungen müssen Sie die migrierten Daten möglicherweise aus Cloud Object Storage in eine andere Cloudspeicherlösung verschieben, beispielsweise [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) oder [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage).  

Weitere Informationen zu Speichermigrationsoptionen finden Sie in [Recipe: Moving data from COS to File or Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}. 

