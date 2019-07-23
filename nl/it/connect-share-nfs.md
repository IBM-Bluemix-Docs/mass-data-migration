---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount NFS share, NFS, access network share, connect to network share

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

# Connessione alla condivisione di rete utilizzando NFS
{: #connect-nfs-share}

Per prepararti per la copia dei dati, puoi accedere alla condivisione di rete sul dispositivo {{site.data.keyword.mdms_full}} utilizzando il protocollo NFS (Network File System).
{: shortdesc}

Prima di connetterti alla condivisione:

- Assicurarsi di avere il software NFS, come ad esempio `nfs-common`, installato sul tuo client. Puoi installare il pacchetto `nfs-common` eseguendo `sudo apt install nfs-common` dalla tua sessione del terminale.

## Gestione dell'accesso alla condivisione NFS
{: #manage-nfs-share-access}

Per impostazione predefinita, la condivisione di rete è impostata per avere un accesso pubblico. Prima di montare la condivisione sul tuo server, puoi aggiungere le regole di accesso NFS sulla condivisione in modo corrispondente ai tuoi requisiti di ambiente o sicurezza. 

Per informazioni dettagliate sul controllo dell'accesso alle condivisioni sul dispositivo di archiviazione, vedi la [documentazione di OSNEXUS QuantaStor](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}.
{: tip}

Per modificare l'accesso alla condivisione NFS:

1. [Accedi all'interfaccia utente del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Nella procedura guidata Common Tasks, fai clic su **View Network Shares** per visualizzare la vista delle condivisioni di rete.

   ![Icone del flusso di lavoro](images/workflow.png)
3. Chiudi la procedura guidata Common Tasks e fai quindi clic con il pulsante destro del mouse sul nome della condivisione di rete per visualizzare un elenco di opzioni. 
4. Fai clic su **Add NFS Access** per modificare l'accesso per la condivisione NFS.

    ![Modifica l'accesso per la condivisione NFS](images/add-nfs-access.png)

## Montaggio della condivisione NFS su un sistema Unix
{: #mount-nfs-share}

Dopo che hai sbloccato e attivato il pool di archiviazione sul dispositivo, puoi connetterti alla condivisione NFS su un sistema basato su Unix utilizzando l'interfaccia utente del dispositivo {{site.data.keyword.mdms_short}}.

Per montare la condivisione di rete: 

1. [Accedi all'interfaccia utente del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. Nella procedura guidata Common Tasks, fai clic su **View Network Shares** per visualizzare la vista delle condivisioni di rete.
3. Chiudi la procedura guidata Common Tasks e fai quindi clic con il pulsante destro del mouse sul nome della condivisione di rete per visualizzare un elenco di opzioni. 
4. Fai clic su **View Mount Command** per esaminare le informazioni di montaggio per la condivisione.

    La seguente immagine mostra la finestra di dialogo View Mount Command con i valori di esempio.

    ![Montaggio della condivisione](images/mount-command.png)

    Il valore _Network Port_ corrisponde alla porta di trasferimento dati sul dispositivo {{site.data.keyword.mdms_short}}. Il valore _Mount command_ specifica il comando utilizzato per montare la condivisione e connettersi a essa.
5. Esegui il ping dell'indirizzo IP elencato nella finestra di dialogo per testare la connettività di rete tra il tuo computer e il dispositivo {{site.data.keyword.mdms_short}}.

   Assicurati che l'indirizzo IP corrisponda alla [porta di trasferimento dati da 10GbE](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings) sul dispositivo.
   {: note}  
6. Copia il comando di montaggio elencato nella finestra di dialogo e incollalo in una sessione di terminale sul tuo computer.
7. Esegui il comando per montare la condivisione sul tuo server.

## Passi successivi
{: #connect-nfs-share-next-steps}

- Avvia il [processo di copia dei dati](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data).
