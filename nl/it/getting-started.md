---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# Esercitazione introduttiva
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} ti aiuta a spostare da terabyte a petabyte di dati in {{site.data.keyword.cloud_notm}} in un modo rapido, semplice e sicuro. Questa esercitazione mostra come richiedere il tuo dispositivo di migrazione utilizzando il {{site.data.keyword.slportal}}.
{: shortdesc}

Interessato a provare le nuove funzioni di {{site.data.keyword.mdms_short}}? Puoi visualizzare in anteprima i miglioramenti del servizio in arrivo partecipando al programma beta di {{site.data.keyword.mdms_short}}. Per ulteriori informazioni, vedi [Come accedere alla versione beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: tip}

## Prima di cominciare
{: #get-started-prereqs}

Prima di ordinare un dispositivo {{site.data.keyword.mdms_short}}:

- Pianifica la tua migrazione controllando le [regioni e le ubicazioni](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions) dove è disponibile {{site.data.keyword.mdms_short}}.
- Assicurati di disporre di un'istanza di cui è stato eseguito il provisioning di [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} per il tuo account {{site.data.keyword.cloud_notm}}. 
- Comprendi i tuoi tipi e le tue velocità di connessione di rete.
- Raccogli le tue impostazioni della rete, quali gli indirizzi IP e altri dettagli di instradamento, per connettere il dispositivo al tuo server di origine.
- Identifica una persona che può ricevere, connettere e utilizzare il dispositivo presso la tua sede.

## Creazione di un bucket di archiviazione
{: #get-started-create-bucket}

Dopo che hai eseguito il provisioning di un'istanza di Cloud Object Storage, crea un bucket di archiviazione per impostare una destinazione per i tuoi dati migrati. 

1. Dall'elenco risorse {{site.data.keyword.cloud_notm}}, seleziona la tua istanza di cui è stato eseguito il provisioning di Cloud Object Storage.
2. Dalla pagina _Introduzione_, fai clic su **Crea bucket**.
3. Immetti un nome di bucket e seleziona un'opzione di resilienza per i tuoi dati.
   
   L'opzione di resilienza determina il modo in cui i tuoi dati vengono distribuiti dal servizio Cloud Object Storage in un'area geografica dopo che i dati sono stati importati nel servizio. {{site.data.keyword.mdms_short}} supporta tutte le opzioni di resilienza che sono disponibili per Cloud Object Storage.  
   {: note}
4. Dall'elenco di ubicazioni, seleziona l'area geografica in cui desideri che i tuoi dati siano fisicamente archiviati dopo essere stati migrati nel bucket di archiviazione.
5. Dall'elenco di classi di archiviazione, seleziona **Standard**.
6. Fai clic su **Crea bucket**.

## Richiesta di un dispositivo
{: #get-started-request-device}

Puoi richiedere un dispositivo {{site.data.keyword.mdms_short}} utilizzando il {{site.data.keyword.slportal}}.

1. Accedi al [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}.
2. Dal menu di navigazione, fai clic su **Storage** > **Data Migration** > **{{site.data.keyword.mdms_short}}** per accedere alla pagina di destinazione di {{site.data.keyword.mdms_short}}.
3. Fai clic su **Request Device** per aprire il modulo d'ordine.
4. Avvia la tua richiesta {{site.data.keyword.mdms_short}} specificando i seguenti dettagli.

    <table>
      <tr>
        <th>Azione</th>
        <th>Descrizione</th>
      </tr>
      <tr>
        <td>Aggiungi un nome richiesta</td>
        <td>Immetti un alias per identificare e tenere traccia della tua richiesta {{site.data.keyword.mdms_short}}.</td>
      </tr>
      <tr>
        <td>Seleziona la tua destinazione di offload dei dati</td>
        <td>Dall'elenco a discesa, seleziona la tua istanza di provisioning di Cloud Object Storage. Quindi, seleziona il nome assegnato al bucket di archiviazione in cui desideri archiviare i tuoi dati migrati.</td>
      </tr>
      <tr>
        <td>Aggiungi un indirizzo di spedizione</td>
        <td>Immetti le tue informazioni di spedizione, come l'indirizzo di spedizione e il nome della persona che accetterà la consegna.</td>
      </tr>
      <tr>
        <td>Aggiungi i contatti di migrazione</td>
        <td>Immetti il nome della persona che gestirà la migrazione dei dati al tuo dispositivo.</td>
      </tr>
      <tr>
        <td>Configura le impostazioni di rete</td>
        <td>
          <p>Configura le impostazioni per la connessione di trasferimento dati immettendo i tuoi dettagli di configurazione della rete.</p>
          <p>Fornisci le seguenti <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">impostazioni di rete</a>:</p>
          <p>
            <ul>
              <li><i>Impostazioni di gestione del dispositivo.</i> Immetti l'indirizzo IP statico, la maschera di rete e il gateway predefinito per il tuo computer remoto.</li>
              <li><i>Impostazioni di trasferimento dati.</i> Immetti l'indirizzo IP statico e la maschera di rete per il server dove si trovano i tuoi dati di origine.</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">Tabella 1. Descrive il flusso di lavoro della richiesta {{site.data.keyword.mdms_short}}</caption>
    </table>

    Quando selezioni un'ubicazione di consegna per il tuo dispositivo, considera il peso del dispositivo e l'accessibilità, Il dispositivo, insieme alla sua custodia rigida e alla custodia da viaggio in foam, pesa circa 26 kg (60 libbre). Per aiutarti con il trasporto del dispositivo, la custodia da viaggio è dotata di ruote e di una maniglia a comparsa per una facile manovrabilità.
    {: tip}
5. Leggi l'accordo in materia di servizi {{site.data.keyword.mdms_short}} e seleziona quindi la casella di spunta.
6. Fai clic su **Place Request** per completare il tuo ordine. 

## Cosa viene dopo
{: #get-started-next-steps}

Operazione riuscita! Tutte le operazioni relative alla tua richiesta {{site.data.keyword.mdms_short}} sono state eseguite.

- Per ulteriori informazioni su come tenere traccia del tuo ordine, consulta [Gestione della tua richiesta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Per ulteriori informazioni sulla ricezione e la connessione del tuo dispositivo, consulta [Impostazione del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview).

