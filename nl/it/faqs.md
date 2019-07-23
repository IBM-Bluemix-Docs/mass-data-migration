---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# Domande frequenti (FAQ)
{: #faqs}

Domande frequenti su {{site.data.keyword.mdms_full}}.
{: shortdesc}

## Cos'è {{site.data.keyword.mdms_full_notm}}?
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} è un servizio di trasferimento dati fisico che accelera lo spostamento sicuro di terabyte e petabyte di dati in {{site.data.keyword.cloud_notm}} utilizzando solidi dispositivi di archiviazione portatili con capacità utilizzabile da 120 TB.

## Come inizio a usare {{site.data.keyword.mdms_short}}?
{: #how-to-use-mdms}
{: faq}

Utilizza il [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} per inviare la tua richiesta. Una volta che la tua richiesta viene approvata ed elaborata, il prossimo dispositivo disponibile viene preconfigurato e spedito in base alle tue informazioni di rete e spedizione. 

## Chi dovrebbe utilizzare {{site.data.keyword.mdms_short}}?
{: #who-uses-mdms}
{: faq}

Dai data center e dagli uffici alle ubicazioni remote come le piattaforme petrolifere e le navi, i dispositivi {{site.data.keyword.mdms_short}} sono equipaggiati per funzionare praticamente in qualsiasi ambiente. {{site.data.keyword.mdms_short}} è anche un'ottima alternativa se le opzioni di trasferimento dati via rete sono troppo proibitive in termini di costi, sono lente o non sono disponibili.

## Quanti dati posso trasferire utilizzando {{site.data.keyword.mdms_short}}?
{: #how-much-data}
{: faq}

Non vi è praticamente alcun limite alla quantità di dati che puoi trasferire, che si tratti di pochi terabyte che di molti petabyte. Ogni dispositivo può contenere fino a 120 TB di capacità utilizzabile con RAID-6, ma puoi utilizzare più dispositivi per gestire carichi di lavoro più grandi. {{site.data.keyword.mdms_short}} offre anche una compressione inline, che può aumentare ulteriormente la capacità utilizzabile a seconda di quanto è comprimibile il tuo dataset. L'oggetto singolo più grande è limitato a una dimensione di 10 TB.


## Come posso utilizzare più dispositivi per spostare carichi di lavoro più grandi che superano i 120 TB?
{: #using-multiple-devices}
{: faq}

Utilizza più dispositivi in parallelo o in serie per spostare tutti i dati in un'unica migrazione o utilizza un singolo dispositivo nelle migrazioni iterative. Ad esempio, trasferisci 1 PB di dati utilizzando nove dispositivi in parallelo o utilizza un singolo dispositivo in nove migrazioni separate. Se utilizzi più dispositivi in parallelo, tieni presente che la velocità di inserimento sarà più lenta.

## Quanto tempo ci vuole per trasferire i miei dati?
{: #transfer-timeline}
{: faq}

Dal momento in cui un cliente inoltra una richiesta {{site.data.keyword.mdms_short}} a quando i suoi dati sono accessibili nel suo bucket IBM Cloud Object Storage, il tempo impiegato può essere una questione di giorni. Le prestazioni del trasferimento possono essere influenzate da molti fattori come la rete, la larghezza di banda o il numero di file che viene trasferito. Ad esempio, il trasferimento di milioni di file di piccole dimensioni durerà più a lungo della stessa quantità di dati contenuta in un numero relativamente inferiore di file più grandi.

## Per quanto tempo posso avere un dispositivo {{site.data.keyword.mdms_short}}?
{: #device-onsite-time}
{: faq}

Un dispositivo può essere tenuto in loco senza alcun costo aggiuntivo per i primi 10 giorni lavorativi. Questo non include il giorno in cui il tuo dispositivo viene spedito né il giorno in cui il tuo dispositivo viene restituito a IBM (massimo di 2 giorni). Se è necessario ulteriore tempo per completare il tuo inserimento puoi, successivamente, estendere il tuo utilizzo per 30 USD per ogni giorno di calendario. Si applica a tutte le regioni.

## Quali interfacce di rete sono supportate da {{site.data.keyword.mdms_short}}?
{: #supported-network-interfaces}
{: faq}

I dispositivi {{site.data.keyword.mdms_short}} dispongono di interfacce di rete a 10-Gbps con porte di rete in rame RJ45 (CAT6a) e SFP+.

I convertitori RJ45 a SFP+ sono inclusi solo con i modelli di dispositivo a cui mancano le connessioni native SFP+. Attualmente la fibra non è supportata.

## Qual è l'opzione di spedizione predefinita per {{site.data.keyword.mdms_short}}?
{: #shipping-options}
{: faq}

{{site.data.keyword.mdms_short}} utilizza la spedizione di andata e ritorno UPS Next Day Air per spedire tutti i dispositivi. Il costo è incluso nella conveniente tariffa forfettaria di 395 USD per dispositivo. Attualmente, i clienti non possono scegliere metodi di spedizione alternativi.


## In quali regioni è disponibile {{site.data.keyword.mdms_short}}?
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}} è attualmente disponibile negli Stati Uniti (USA) e in Unione Europea (UE), Giappone, Australia, Brasile, Singapore, Hong Kong, Norvegia, Corea del Sud, Canada e Messico. È in corso un'ulteriore espansione geografica. L'ordinazione online è disponibile nella maggior parte delle regioni. Per le eventuali regioni senza l'ordinazione online, contatta il tuo rappresentante delle vendite IBM per chiedere in merito all'utilizzo del servizio.

I dispositivi non possono essere spediti attraverso i confini internazionali (ad esempio, un dispositivo non può essere ordinato in una regione e spedito in un'altra regione), fatta eccezione per l'Unione Europea e i suoi 28 paesi membri.
{: note}

## Qual è l'opzione di spedizione predefinita per {{site.data.keyword.mdms_short}} negli Stati Uniti?
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}} utilizza la spedizione con consegna il giorno successivo UPS andata e ritorno per i dispositivi degli Stati Uniti. Il costo di spedizione è incluso nel prezzo. I clienti attualmente non possono selezionare dei metodi di spedizione alternativi. 

## Qual è l'opzione di spedizione predefinita per {{site.data.keyword.mdms_short}} nell'Unione Europea?
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}} utilizza la spedizione con consegna il giorno successivo FedEx andata e ritorno per i dispositivi dell'Unione Europea. Il costo di spedizione è incluso nel prezzo. I clienti attualmente non possono selezionare dei metodi di spedizione alternativi. 

## Qual è l'opzione di spedizione predefinita {{site.data.keyword.mdms_short}} in tutte le altre regioni supportate?
{: #default-shipping-other}
{: faq}

Per tutte le regioni supportate al di fuori degli Stati Uniti e dell'UE, i fornitori di spedizione e i tempi complessivi di spedizione varieranno. Il costo di spedizione è incluso nel prezzo. I clienti attualmente non possono selezionare dei metodi di spedizione alternativi.

In queste regioni, IBM non è in grado di prenotare la spedizione andata e ritorno quando effettui il tuo ordine. Vengono invece prenotate delle spedizioni unidirezionali quando è necessaria una spedizione. Per le spedizioni in uscita, concedi almeno tre giorni lavorativi perché IBM coordini la spedizione del tuo dispositivo {{site.data.keyword.mdms_short}} dopo che hai effettuato la tua richiesta.
{: note}

Per gli ordini non degli Stati Uniti e non dell'Unione Europea, richiedi una spedizione di restituzione per il dispositivo almeno tre giorni lavorativi prima della data in cui desideri spedire il dispositivo. Ad esempio, se vuoi spedire il dispositivo di venerdì, coordina una spedizione di restituzione il lunedì della stessa settimana. Puoi chiedere una spedizione di restituzione dalla scheda _Request details_ nel dashboard {{site.data.keyword.mdms_short}}.
{: important}

## Sono in Giappone, Australia, Brasile, Canada, Messico, Hong Kong, Singapore, Norvegia o Corea del Sud. Come richiedo la spedizione di restituzione per il mio dispositivo {{site.data.keyword.mdms_short}}?
{: #shipping-timetable-other}
{: faq}

Se stai utilizzando {{site.data.keyword.mdms_short}} fuori dalle regioni Stati Uniti e Unione Europea, devi richiedere una spedizione di restituzione per il dispositivo almeno tre giorni lavorativi prima della data in cui vuoi spedire il dispositivo. Ad esempio, se vuoi spedire il dispositivo di venerdì, coordina una spedizione di restituzione il lunedì della stessa settimana.

## Quanto costa importare i dati in {{site.data.keyword.cloud_notm}}?
{: #data-transfer-cost}
{: faq}

Non viene addebitato alcun costo per i dati trasferiti in {{site.data.keyword.cloud_notm}}.


## Posso utilizzare {{site.data.keyword.mdms_short}} per esportare i dati da {{site.data.keyword.cloud_notm}}?
{: #exporting-data}
{: faq}

Attualmente, {{site.data.keyword.mdms_short}} non supporta l'esportazione di dati da {{site.data.keyword.cloud_notm}}.


## {{site.data.keyword.mdms_short}} crittografa i miei dati?
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}} crittografa tutti i dati con la crittografia AES a 256 bit e fornisce una password complessa per sbloccare il pool di archiviazione. Tutti i trasferimenti di dati all'interno di {{site.data.keyword.IBM}} avvengono su SSL.

## In che modo {{site.data.keyword.mdms_short}} protegge fisicamente i miei dati?
{: #security}
{: faq}

Tutti i dispositivi {{site.data.keyword.mdms_short}} sono alloggiati in custodie robuste e resistenti. Queste custodie sono impermeabili, resistenti agli urti e a prova di manomissione per proteggere il dispositivo nei viaggi di andata e ritorno e per la sicurezza dei dati.

## Come posso tracciare la mia richiesta durante il processo di migrazione?
{: #how-to-track-request}
{: faq}

Per tenere traccia dello stato della tua richiesta, vai alla scheda _Request details_ nel dashboard {{site.data.keyword.mdms_short}} nella console {{site.data.keyword.cloud_notm}}.

## Come vengono cancellati i miei dati dal dispositivo {{site.data.keyword.mdms_short}} dopo che sono stati scaricati in {{site.data.keyword.cos_full_notm}}?
{: #data-erasure}
{: faq}

Una volta completato il tuo offload dei dati a IBM Cloud Object Storage, IBM cancella immediatamente i dati sul dispositivo utilizzando gli standard di cancellazione dei dati NIST per garantire una cancellazione completa di tutti i dati del cliente dai dispositivi.

## Quali sono le interfacce file su {{site.data.keyword.mdms_short}}?
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} supporta i protocolli NFS (Network File System) e SMB (Server Message Block).

## Come utilizzo l'interfaccia file su {{site.data.keyword.mdms_short}}?
{: #how-to-use-file-interface}
{: faq}

Per prima cosa, sblocca il pool di crittografia. Successivamente, monta la condivisione sul server che contiene i dati che intendi migrare. Inizia a copiare i tuoi file di dati nella condivisione di rete.

## Quali sono i vantaggi dell'interfaccia file su {{site.data.keyword.mdms_short}}?
{: #file-interface-benefits}
{: faq}

L'interfaccia di file è basata su un software di rete e file evoluto che consente di copiare e trasportare un elevato numero di file di grandi dimensioni su {{site.data.keyword.cloud_notm}}.

## Come vengono archiviati i file sul dispositivo {{site.data.keyword.mdms_short}}?
{: #file-storage}
{: faq}

I dispositivi {{site.data.keyword.mdms_short}} utilizzano un file system ZFS con compressione LZ4 e crittografia AES a 256 bit.

## Quanto costa utilizzare {{site.data.keyword.mdms_short}} negli Stati Uniti?
{: #pricing-us}
{: faq}

Negli Stati Uniti, viene addebitata una tariffa forfettaria di 395 USD per ogni dispositivo, che include il costo del dispositivo di 295 USD, la spedizione con consegna il giorno successivo UPS andata e ritorno di 100 USD e 10 giorni lavorativi di utilizzo presso la tua sede.

I tuoi 10 giorni di utilizzo in sede non includono il giorno in cui il dispositivo ti viene spedito e il giorno in cui il tuo dispositivo viene restituito a IBM (massimo di due giorni). Se occorre più tempo per completare la tua migrazione oltre ai 10 giorni lavorativi assegnati, ti verrà addebitata un'estensione di 30 USD al giorno per ogni giorno di utilizzo aggiuntivo.

## Quanto costa utilizzare {{site.data.keyword.mdms_short}} nell'UE?
{: #pricing-eu}
{: faq}

Nell'Unione Europea, viene addebitata una tariffa forfettaria di 445 USD per ogni dispositivo, che include il costo del dispositivo di 295 USD, la spedizione con consegna il giorno successivo FedEx andata e ritorno di 150 USD e 10 giorni lavorativi di utilizzo presso la tua sede.

I tuoi 10 giorni di utilizzo in sede non includono il giorno in cui il dispositivo ti viene spedito e il giorno in cui il tuo dispositivo viene restituito a IBM (massimo di 2 giorni). Se occorre più tempo per completare la tua migrazione oltre ai 10 giorni assegnati, ti verrà addebitata un'estensione di 30 USD al giorno per ogni giorno di utilizzo aggiuntivo.

## Quanto costa utilizzare {{site.data.keyword.mdms_short}} in tutte le altre regioni supportate?
{: #pricing-other}
{: faq}

In tutte le altre regioni (Giappone, Australia, Brasile, Canada, Messico, Hong Kong, Singapore, Norvegia e Corea del Sud), viene addebitata una tariffa forfettaria di 1,145 USD per ogni dispositivo, che include il costo del dispositivo di 295 USD, la spedizione andata e ritorno di 850 USD e 10 giorni lavorativi di utilizzo presso la tua sede.

I tuoi 10 giorni di utilizzo in sede non includono il giorno in cui il dispositivo ti viene spedito e il giorno in cui il tuo dispositivo viene restituito a IBM (un massimo di 2 giorni). Se occorre più tempo per completare la tua migrazione oltre ai 10 giorni assegnati, ti verrà addebitata un'estensione di 30 USD al giorno per ogni giorno di utilizzo aggiuntivo.

Ci sono dei requisiti di spedizione speciali per queste regioni. Per ulteriori informazioni, vedi sopra.
{: note}

## Mi viene addebitato l'uso di {{site.data.keyword.cos_full_notm}}?
{: #pricing-cos}
{: faq}

Il trasferimento di dati in {{site.data.keyword.cloud_notm}} viene eseguito senza alcun addebito a tuo carico. Tuttavia, verranno applicate tariffe standard per i dati archiviati in {{site.data.keyword.cos_full_notm}} o in qualsiasi altro servizio {{site.data.keyword.cloud_notm}}. Per ulteriori informazioni sulle opzioni di prezzo in Cloud Object Storage, vedi la sezione dedicata ai [prezzi di {{site.data.keyword.cos_full_notm}}](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}. 

## Posso comprare un dispositivo {{site.data.keyword.mdms_full_notm}}?
{: #purchasing-devices}
{: faq}

I dispositivi {{site.data.keyword.mdms_full_notm}} non sono disponibili per l'acquisto.

## In che modo il processo {{site.data.keyword.mdms_short}} mantiene l'univocità dei nomi oggetto?
{: #object-name-uniqueness}
{: faq}

Per garantire che i nomi oggetto siano univoci quando vengono copiati in un bucket Cloud Object Storage, al percorso file viene incluso un prefisso nel nome oggetto. Ad esempio, `/root/user/config.ini` diventa `root/user/config.ini` quando viene copiato nel bucket.

## Cosa succede se il bucket di destinazione non esiste nell'account {{site.data.keyword.cos_full_notm}}?
{: #target-buckets}
{: faq}

Se non esiste, il bucket di destinazione viene creato. Se esiste, deve essere vuoto, altrimenti la copia non può procedere.  

## I collegamenti vengono ignorati durante il processo di scansione?
{: #links-scan-process}
{: faq}

Sì. I collegamenti simbolici e i collegamenti reali vengono ignorati durante il processo di scansione.
