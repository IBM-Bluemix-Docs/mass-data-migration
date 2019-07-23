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

# Verifica dei tuoi dati
{: #verify-data}

Puoi accedere ai tuoi dati migrati e verificarli utilizzando {{site.data.keyword.cos_full}}.
{: shortdesc}

Una volta che l'offload è stato completato, accedi immediatamente ai tuoi dati nel cloud mentre {{site.data.keyword.cloud_notm}} cancella il dispositivo in tutta sicurezza.

## Accesso ai tuoi dati in Cloud Object Storage
{: #access-data-cos}

I tuoi dati migrati sono disponibili nell'istanza Storage Object Storage che hai specificato quando hai inoltrato la tua richiesta {{site.data.keyword.mdms_short}}. Prima di eliminare i dati dal tuo server di origine, verifica che siano stati caricati correttamente su {{site.data.keyword.cloud_notm}}.

Per accedere ai tuoi dati e verificarli: 

1. [Accedi alla console {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Vai a **Menu** &gt; **Elenco risorse** per visualizzare un elenco delle tue risorse.
3. Dal tuo elenco risorse {{site.data.keyword.cloud_notm}}, seleziona l'istanza di cui è stato eseguito il provisioning di Cloud Object Storage.
4. Dall'elenco di bucket di archiviazione disponibili, seleziona il nome bucket che hai designato per la migrazione dei dati.
5. Verifica che gli oggetti associati al bucket corrispondano ai dati che hai copiato sul dispositivo {{site.data.keyword.mdms_short}}.

## Spostamento dei dati a una soluzione di archiviazione diversa
{: #move-data}

A seconda dei tuoi requisiti di carico di lavoro, potresti aver bisogno di spostare i tuoi dati migrati da Cloud Object Storage a una soluzione di archiviazione cloud differente, come ad esempio [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) o [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage). 

Per ulteriori informazioni sulle opzioni di migrazione di archiviazione, consulta [Recipe: Moving data from COS to File or Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}.

