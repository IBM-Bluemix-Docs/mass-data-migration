---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# Risoluzione dei problemi
{: #troubleshooting}

I problemi generali con l'utilizzo di {{site.data.keyword.mdms_full}} potrebbero includere la visualizzazione dello stato dell'ordine o l'accesso all'interfaccia utente. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{: shortdesc}

## Impossibile connettersi alla condivisione SMB
{: #unable-to-mount-smb-share}

Quando provi a montare la condivisione SMB (Server Message Block) di cui viene eseguito il provisioning sul dispositivo {{site.data.keyword.mdms_short}}, non sei in grado di connetterti alla condivisione. 

Stai utilizzando il protocollo di trasferimento file SMB su un server Windows che è unito a un dominio Active Directory. Per spostare i dati nel dispositivo {{site.data.keyword.mdms_short}}, devi connetterti alla condivisione di rete di cui è stato eseguito il provisioning nel dispositivo. Puoi eseguire il ping dell'indirizzo IP che corrisponde alla porta di trasferimento dati da 10GbE sul dispositivo ma non riesci a montare la condivisione o a connetterti a essa dal tuo server.
{: tsSymptoms}

Dopo che hai unito il dispositivo {{site.data.keyword.mdms_short}} ad Active Directory, il sistema abilita la firma SMB per impostazione predefinita. La firma SMB aggiunge una sicurezza supplementare durante le comunicazioni di rete eliminando la possibilità di attacchi man-in-the-middle. Tuttavia, la firma SMB può avere delle ripercussioni sulle prestazioni di rete per il tuo trasferimento dati o causare dei [problemi al momento del montaggio della condivisione al tuo server](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}.
{: tsCauses} 

Se non utilizzi la firma SMB per il tuo ambiente, o non ne hai bisogno, puoi disabilitarla sul client per evitare problemi di connessione e aumentare le prestazioni del tuo trasferimento dati.
{: tsResolve}

Per disabilitare la firma SMB su un server Windows, imposta le seguenti chiavi di registro su zero:

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000
```
{: screen}

Per ulteriori informazioni sulla firma SMB, vedi il documento di [panoramica della firma Server Message Block](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}.

## Impossibile visualizzare i dettagli dell'ordine
{: #unable-to-view-order}

Quando accedi alla console {{site.data.keyword.cloud_notm}}, non puoi visualizzare o tracciare un ordine {{site.data.keyword.mdms_short}} per la tua organizzazione.

Puoi visualizzare un elenco dei servizi nel tuo elenco risorse {{site.data.keyword.cloud_notm}} ma non puoi visualizzare una voce {{site.data.keyword.mdms_short}}.
{: tsSymptoms}

Non disponi dell'autorizzazione corretta per visualizzare o tracciare gli ordini {{site.data.keyword.mdms_short}}.
{: tsCauses} 

Verifica con il tuo amministratore che ti sia stato assegnato il ruolo corretto nel gruppo di risorse o nell'istanza del servizio applicabile. er ulteriori informazioni sui ruoli, vedi [Ruoli e autorizzazioni](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Come ottenere aiuto e supporto
{: #getting-help}

Se hai problemi o domande quando stai utilizzando il tuo dispositivo {{site.data.keyword.mdms_short}}, puoi ottenere aiuto ricercando le informazioni nel Centro di supporto o contattandoci direttamente.

Per accedere al Centro di supporto, esegui l'accesso alla console {{site.data.keyword.cloud_notm}} e fai clic su **Supporto** dalla barra dei menu.

Puoi utilizzare il campo di ricerca del Centro di supporto per trovare risposte alle tue domande attraverso la documentazione {{site.data.keyword.cloud_notm}} e il forum Stack Overflow. Dal Centro di supporto, puoi anche gestire i casi di supporto. Puoi trovare collegamenti sia al forum Stack Overflow per le domande tecniche che al forum IBM Developer Answers per tutte le altre domande sotto la sezione Forum del Centro di supporto.

Se hai un [piano di supporto](/docs/get-support?topic=get-support-support-plans#support-plans) di base, avanzato o premium, puoi trovare i numeri da chiamare e un'opzione di chat per ottenere assistenza.

Il Centro di supporto è il metodo preferito per ottenere supporto ma, se non riesci ad accedere a {{site.data.keyword.cloud_notm}}, puoi utilizzare l'[Service Portal{{site.data.keyword.cloud_notm}}](http://www.ibm.biz/bluemixsupport){: external} per inoltrare un caso.

Per ulteriori informazioni sull'apertura di un ticket di supporto {{site.data.keyword.IBM_notm}} o sui livelli di supporto e sulle severità dei ticket, vedi [Come contattare il supporto](/docs/get-support?topic=get-support-getting-customer-support){: external}.
