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

# Sblocco del pool di archiviazione
{: #unlock-storage-pool}

Puoi copiare i dati nel dispositivo {{site.data.keyword.mdms_full}} sbloccando e attivando prima il pool di archiviazione di cui viene eseguito il provisioning per il dispositivo.
{: shortdesc}

## Richiamo della passphrase del pool di archiviazione (beta)
{: #retrieve-storage-pool-passcode}

Per accedere al pool di archiviazione sul dispositivo {{site.data.keyword.mdms_short}}, richiama le tue credenziali del dispositivo andando ai dettagli della richiesta {{site.data.keyword.mdms_short}} nella console {{site.data.keyword.cloud_notm}}.

Questa funzione è disponibile come parte della [release beta di {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). Puoi anche accedere alle credenziali per il tuo dispositivo di archiviazione dalla sezione _Request Details_ nel [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Per richiamare la tua passphrase del pool di archiviazione:

1. [Accedi alla console {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Vai a **Menu** &gt; **Elenco risorse** per visualizzare un elenco delle tue risorse.
3. Dal tuo elenco risorse {{site.data.keyword.cloud_notm}}, seleziona l'istanza di cui è stato eseguito il provisioning di {{site.data.keyword.mdms_short}}.
4. Nella scheda _Request details_, vai alla sezione Credentials.
5. Copia il valore **Pool lock passcode**.

## Attivazione del pool di archiviazione
{: #activate-storage-pool}

Sblocca il pool di archiviazione vuoto utilizzando le credenziali che hai richiamato nel passo precedente.

1. [Accedi all'interfaccia utente del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Nella procedura guidata Common Tasks, fai clic su **Unlock and Start Storage Pool**.
3. Immetti la passphrase del pool di archiviazione che hai richiamato nel passo 1 e fai quindi clic su **OK**.
      
   ![Attiva pool di archiviazione](/images/StartStoragePool.png)

   Per impostazione predefinita, la condivisione ha entrambi i protocolli NFS (Network File System) e SMB (Server Message Block) che sono abilitati senza limitazioni dell'accesso. Puoi modificare l'accesso a questa condivisione per NFS o SMB facendo clic con il pulsante destro del mouse sul nome della condivisione nell'interfaccia utente e selezionando quindi l'opzione di menu appropriata.
   {: note}

## Passi successivi
{: #unlock-storage-pool-next-steps}

- Se stai utilizzando una macchina Unix, [connettiti alla condivisione di rete utilizzando NFS](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share).
- Se stai utilizzando una macchina Windows, [connettiti alla condivisione di rete utilizzando SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share).
- Avvia il [processo di copia dei dati](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy).
