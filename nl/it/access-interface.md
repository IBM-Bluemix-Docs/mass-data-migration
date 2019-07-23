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

# Accesso all'interfaccia utente del dispositivo
{: #access-ui}

Dopo che hai configurato il dispositivo {{site.data.keyword.mdms_full}} per la connettività Ethernet, sei pronto ad accedere all'interfaccia utente del dispositivo in modo da poter interagire con il dispositivo e iniziare il processo di migrazione dei dati.
{: shortdesc}

## Richiamo delle tue credenziali di dispositivo (beta)
{: #retrieve-device-credentials}

Quando inoltri una richiesta {{site.data.keyword.mdms_short}}, il servizio genera automaticamente le credenziali per tuo conto, che puoi utilizzare per accedere all'IU web locale per il dispositivo. 

Questa funzione è disponibile come parte della [release beta di {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). Puoi anche accedere alle credenziali per il tuo dispositivo di archiviazione dalla sezione _Request Details_ nel [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Per richiamare le tue credenziali del dispositivo:

1. [Accedi alla console {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Vai a **Menu** &gt; **Elenco risorse** per visualizzare un elenco delle tue risorse.
3. Dal tuo elenco risorse {{site.data.keyword.cloud_notm}}, seleziona l'istanza di cui è stato eseguito il provisioning di {{site.data.keyword.mdms_short}}.
4. Nella scheda _Request details_, vai alla sezione Credentials.
5. Copia i valori di **User name** e **Password**.

## Accesso all'interfaccia utente del dispositivo
{: #log-in-ui}

Utilizza le credenziali del dispositivo richiamate nel passo precedente per accedere all'interfaccia utente web locale e interagire con il dispositivo {{site.data.keyword.mdms_short}}.

1. Apri un browser web e vai all'indirizzo IP statico che hai fornito nel modulo di ordine.

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Sostituisci `<device_management_IP_address>` con l'indirizzo IP configurato per le tue porte di rete Eth1 o Eth2. Accetta l'eccezione del certificato.

2. Accedi al'IU del dispositivo utilizzando il nome utente e la password che hai richiamato nel passo precedente. 

   ![Pagina di accesso](images/login.png)
   
   Viene visualizzata la procedura guidata Common Tasks. Utilizza le opzioni da sinistra a destra per iniziare a importare i tuoi dati.

   ![Icone del flusso di lavoro](images/workflow.png)

   Puoi riaprire la procedura guidata Common Tasks utilizzando il **Workflow Manager** nell'area superiore sinistra dell'interfaccia.
   {:tip}

## Passi successivi
{: #access-ui-next-steps}

- Per prepararti per la copia di inserimento dati, inizia [sbloccando il pool di archiviazione sul dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool).
