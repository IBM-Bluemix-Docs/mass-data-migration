---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

# Gestione della tua richiesta
{: #manage-request}

Gestisci e tieni traccia dello stato del tuo ordine {{site.data.keyword.mdms_full}} utilizzando il {{site.data.keyword.slportal}}.
{: shortdesc}

Partecipando al programma beta di {{site.data.keyword.mdms_short}}, puoi visualizzare in anteprima un nuovo dashboard del servizio {{site.data.keyword.mdms_short}} a cui puoi accedere dalla console {{site.data.keyword.cloud_notm}}. Per ulteriori informazioni, vedi [Come accedere alla versione beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Traccia del tuo ordine 
{: #track-order}

Dopo che hai richiesto un dispositivo di archiviazione, puoi tenere traccia dell'avanzamento del tuo ordine utilizzando la [pagina dei dettagli della richiesta{{site.data.keyword.mdms_short}}](https://control.softlayer.com/storage/mdms){: external} disponibile dal {{site.data.keyword.slportal}}.

La seguente tabella mostra come varia lo stato dell'ordine man mano che {{site.data.keyword.mdms_short}} elabora la richiesta.

| Stato | Descrizione |
| --- | --- |
| Processing Request | Dopo che {{site.data.keyword.mdms_short}} riceve la richiesta, lo stato viene modificato in _Processing request_. |
| Prepping Device | Dopo che il tuo ordine è stato approvato, lo stato della richiesta viene modificato in _Prepping device_. {{site.data.keyword.mdms_short}} prepara e configura il successivo dispositivo di archiviazione disponibile.  |
| Awaiting Shipment | Il dispositivo di archiviazione preconfigurato è in attesa di spedizione alla tua ubicazione. Dopo essere passato allo stato _Awaiting shipment_, l'ordine non può più essere annullato. |
| Device Shipped | Il dispositivo di archiviazione viene ritirato dallo spedizioniere e spedito alla tua ubicazione. Puoi visualizzare il numero di tracciabilità nella sezione _Order Details_ della [pagina dei dettagli della richiesta](https://control.softlayer.com/storage/mdms){: external}. |
| Device Received | Dopo che il dispositivo è stato restituito a {{site.data.keyword.cloud_notm}}, lo stato viene modificato in _Device Received_. |
| Offloading Data | Durante il processo di trasferimento dati, lo stato della richiesta viene modificato in _Offloading Data_. Il dispositivo è connesso alla rete nel data center {{site.data.keyword.cloud_notm}} e l'offload dei dati viene avviato automaticamente. |
| Offload Complete| Quando il processo di offload è completo, lo stato della richiesta viene modificato in _Offload complete_. I tuoi dati sono ora disponibili nella destinazione Cloud Object Storage che hai specificato nella richiesta iniziale. |
| Erase Complete | {{site.data.keyword.mdms_short}} cancella in modo permanente i dati dal dispositivo utilizzando gli standard di cancellazione dei dati NIST. Dopo che il processo di cancellazione dei dati è completo, lo stato dell'ordine viene modificato in _Erase Complete_.
{: caption="Tabella1. Descrive il flusso di lavoro dello stato dell'ordine {{site.data.keyword.mdms_short}}" caption-side="top"}
