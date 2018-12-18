---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-05"

---
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# Domande frequenti (FAQ)

## Cos'è {{site.data.keyword.cloud_notm}} Mass Data Migration?

{{site.data.keyword.cloud}} Mass Data Migration è un servizio di trasferimento dati fisico che accelera il trasferimento sicuro di terabyte e petabyte di dati in {{site.data.keyword.cloud_notm}} utilizzando solidi dispositivi di archiviazione portatile con capacità utilizzabile da 120 TB.

<hr/>

## Come avvio Mass Data Migration?
{: faq}

Utilizza il [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} per inviare la tua richiesta. Una volta che la tua richiesta viene approvata ed elaborata, il prossimo dispositivo disponibile viene preconfigurato e spedito in base alle tue informazioni di rete e spedizione. Utilizza il seguente link per iniziare subito: https://control.softlayer.com/storage/mdms

<hr/>

## Perché utilizzare Mass Data Migration?
{: faq}

I dispositivi Mass Data Migration sono in grado di funzionare in quasi tutti gli ambienti: da data center e uffici a ubicazioni remote, magazzini e navi. Mass Data Migration è anche un'alternativa se le opzioni di trasferimento dati via rete sono proibitive in termini di costo, troppo lente o non disponibili.

<hr/>

## Quanti dati è possibile trasferire utilizzando Mass Data Migration?

Non vi è praticamente alcun limite alla quantità di dati che puoi trasferire, che si tratti di pochi terabyte o di petabyte. Ogni dispositivo può contenere fino a 120 TB di capacità utilizzabile con RAID-6, ma puoi utilizzare più dispositivi per gestire carichi di lavoro più grandi. L'oggetto singolo più grande è limitato a 10 TB.

<hr/>

## Possono essere utilizzati più dispositivi per spostare i carichi di lavoro più grandi che superano i 120 TB? Se sì, come?
{: faq}

Utilizza più dispositivi in parallelo o in serie per spostare tutti i dati in un'unica migrazione o utilizza un singolo dispositivo nelle migrazioni iterative. Ad esempio, trasferisci 1 PB di dati utilizzando nove dispositivi in parallelo o utilizza un singolo dispositivo in nove migrazioni separate.

<hr/>

## Quanto tempo ci vuole per trasferire i dati?
{: faq}

Dal momento in cui un cliente invia una richiesta per Mass Data Migration a quando i suoi dati sono accessibili nel proprio bucket di {{site.data.keyword.cos_full}}, il tempo complessivo può essere di appena sette giorni. Le prestazioni di trasferimento sono influenzate dal numero di file che devono essere trasferiti. Il trasferimento di milioni di file di piccole dimensioni ha una durata superiore rispetto alla stessa quantità di dati contenuta in relativamente meno file.

<hr/>

## Per quanto tempo il dispositivo Mass Data Migration può essere conservato?

Un dispositivo può essere tenuto in loco gratuitamente per i primi 10 giorni lavorativi. Questo intervallo di tempo non include il giorno in cui il dispositivo viene spedito o il giorno in cui lo ricevi. Se è necessario ulteriore tempo per completare il tuo inserimento, puoi estendere l'utilizzo per 30 dollari americani (USD) al giorno (valido per le regioni degli Stati Uniti e dell'UE).

<hr/>

## Quali interfacce di rete sono supportate da Mass Data Migration?
{: faq}

I dispositivi Mass Data Migration dispongono di interfacce di rete a 10-Gbps con porte di rete in rame RJ45 (CAT6a) e SFP+. Il convertitore da RJ45 a SFP+ è incluso. I frame Jumbo sono abilitati sulle interfacce a 10-Gbps.

<hr/>

## Qual è l'opzione di spedizione predefinita per Mass Data Migration?
{: faq}

Mass Data Migration utilizza la spedizione di andata e ritorno UPS Next Day Air per spedire tutti i dispositivi. Il costo è incluso nella conveniente tariffa forfettaria di 395 USD per dispositivo. Attualmente, i clienti non possono scegliere metodi di spedizione alternativi.

<hr/>

## In quali regioni è disponibile Mass Data Migration?
{: faq}

Mass Data Migration è disponibile solo negli Stati Uniti e nell'Unione europea. Tutti i dati vengono migrati in {{site.data.keyword.cos_full}} nei livelli del servizio degli Stati Uniti in più regioni standard o dell'UE in più regioni. I dispositivi non possono essere spediti da una regione e restituiti a un'altra regione.

<hr/>

## Quanto costa importare i dati in {{site.data.keyword.cloud_notm}}?
{: faq}

Non viene addebitato alcun costo per i dati trasferiti in {{site.data.keyword.cloud_notm}}.

<hr/>

## È possibile utilizzare Mass Data Migration per esportare i dati all'esterno di {{site.data.keyword.cloud_notm}}?
{: faq}

Attualmente, Mass Data Migration non supporta l'esportazione di dati al di fuori di {{site.data.keyword.cloud_notm}}.

<hr/>

## Mass Data Migration crittografa i dati?
{: faq}

Mass Data Migration crittografa tutti i dati con crittografia AES a 256 bit e fornisce una password complessa per sbloccare il pool di archiviazione. Tutti i trasferimenti di dati all'interno di {{site.data.keyword.IBM}} avvengono su SSL.

<hr/>

## In che modo Mass Data Migration protegge fisicamente i dati?
{: faq}

Tutti i dispositivi Mass Data Migration sono alloggiati in custodie robuste e resistenti. Queste custodie sono impermeabili, resistenti agli urti e a prova di manomissione per proteggere il dispositivo nei viaggi di andata e ritorno e per la sicurezza dei dati.

<hr/>

## Come è possibile tracciare la richiesta durante il processo di migrazione?

Per tracciare lo stato della tua richiesta, fai riferimento alla sezione delle richieste attive nella pagina di Mass Data Migration nel [{{site.data.keyword.slportal}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){:new_window}. Puoi accedere al portale utilizzando il seguente link: https://control.softlayer.com/storage/mdms ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")

<hr/>

## Come vengono cancellati i dati dopo che sono stati scaricati in {{site.data.keyword.cos_full_notm}}?

Non appena lo scaricamento dei dati in {{site.data.keyword.cos_full}} viene completato, {{site.data.keyword.IBM}} avvia immediatamente una cancellazione dei dati a livello DOD in quattro passaggi per cancellare in modo permanente i tuoi dati dal dispositivo.

<hr/>

## Cos'è l'interfaccia di file?
{: faq}

Il dispositivo Mass Data Migration dispone di condivisioni con NFS (Network File System) e SMB (Server Message Block) abilitate per impostazione predefinita.

<hr/>

## Come viene utilizzata l'interfaccia di file?
{: faq}

Per prima cosa, sblocca il pool di crittografia. Successivamente, monta la condivisione sul server che contiene i dati che intendi migrare. Avvia la copia dei file di dati nella condivisione.

<hr/>

## Quali sono i vantaggi dell'interfaccia di file su Mass Data Migration?
{: faq}

L'interfaccia di file è basata su un software di rete e file evoluto che consente di copiare e trasportare un elevato numero di file di grandi dimensioni su {{site.data.keyword.cloud_notm}}.

<hr/>

## Come vengono memorizzati i file nel dispositivo Mass Data Migration?
{: faq}

I dispositivi Mass Data Migration utilizzano un file system ZFS con compressione LZ4 e crittografia AES a 256 bit.

<hr/>

## Quanto costa utilizzare Mass Data Migration negli Stati Uniti?
{: faq}

Negli Stati Uniti, viene addebitata una tariffa forfettaria di 395 USD per ogni dispositivo. Questo costo include il costo del dispositivo di 295 USD, la spedizione di andata e ritorno con UPS Next Day Air di 100 USD e 10 giorni lavorativi di utilizzo presso la tua sede.

<hr/>

## Quanto costa l'utilizzo di {{site.data.keyword.cos_full_notm}}?
{: faq}

Il trasferimento dei dati in {{site.data.keyword.cloud_notm}} è gratuito. Tuttavia, verranno applicate tariffe standard per i dati memorizzati in {{site.data.keyword.cos_full}} o in qualsiasi altro servizio {{site.data.keyword.cloud_notm}}. Puoi trovare i prezzi per {{site.data.keyword.cos_full}} per l'offerta in più regioni standard al seguente link: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")

<hr/>

## È possibile acquistare un dispositivo {{site.data.keyword.cloud_notm}} Mass Data Migration?
{: faq}

I dispositivi {{site.data.keyword.cloud_notm}} Mass Data Migration non sono disponibili per l'acquisto.

<hr/>

## Come il processo di {{site.data.keyword.cloud_notm}} Mass Data Migration mantiene l'univocità dei nomi oggetto?
{: faq}

Per garantire che i nomi oggetto siano univoci quando vengono copiati nel bucket, al percorso file viene incluso un prefisso nel nome oggetto. Ad esempio, `/root/user/config.ini` diventa `root/user/config.ini` quando copiato nel bucket.

## Cosa succede se il bucket di destinazione non esiste nell'account {{site.data.keyword.cos_full_notm}}?
{: faq}

Se non esiste, il bucket di destinazione viene creato. Se esiste, deve essere vuoto, altrimenti la copia non può procedere.  

## I collegamenti vengono ignorati durante il processo di scansione?
{: faq}

Sì. I collegamenti simbolici e i collegamenti reali vengono ignorati durante il processo di scansione.
