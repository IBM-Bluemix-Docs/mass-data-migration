---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: region availability, storage locations, storage destinations

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

# Disponibilità regione
{: #regions}

Con {{site.data.keyword.mdms_full}} e {{site.data.keyword.cos_full_notm}}, puoi scegliere tra le diverse opzioni di archiviazione per soddisfare le tue esigenze di disponibilità e resilienza.  
{: shortdesc}

## Regioni supportate
{: #available-regions}

Puoi ordinare un dispositivo {{site.data.keyword.mdms_short}} negli Stati Uniti (USA), in Unione Europea (UE) e in Giapponese, Australia, Brasile, Singapore, Hong Kong, Norvegia, Corea del Sud, Canada e Messico.

Prima di ordinare un dispositivo, tieni presente le seguenti limitazioni di spedizione e trasferimento dati:

- **I dispositivi {{site.data.keyword.mdms_short}} non possono essere spediti attraverso i confini internazionali** (fatta eccezione per l'Unione Europea e i suoi 28 paesi membri). Ad esempio, non puoi importare i dati nel dispositivo in una regione e quindi spedire il dispositivo a un'altra regione.
- **Puoi trasferire i dati solo all'interno del Paese dove risiedono i tuoi dati di origine** (fatta eccezione per Interregionale UE e Interregionale AP), Questo significa che la tua destinazione del bucket Cloud Object Storage deve anche trovarsi nello stesso Paese del data center dove il dispositivo {{site.data.keyword.mdms_short}} verrà preparato per l'offload dei dati. 

## Destinazioni dell'archiviazione 
{: #storage-destinations}

I tuoi dati vengono migrati in Cloud Object Storage, dove puoi scegliere da classi, ubicazioni e resilienza dell'archiviazione differenti per i tuoi dati archiviati. 

{{site.data.keyword.mdms_short}} supporta tutte le opzioni di ubicazioni e resilienza dell'archiviazione disponibili per Cloud Object Storage. La seguente tabella associa ogni Paese con i suoi data center e le opzioni di offload dei dati disponibili.

| Paese | Data center | Destinazioni dell'archiviazione |
|-----|-----|----|
| Brasile | São Paulo | Sito singolo: `sao01`  |
| Canada | Montreal<br>Toronto | Sito singolo: `mon01` <br> Sito singolo: `tor01` |
| Messico| Città del Messico | Sito singolo: `mex01` |
| Stati Uniti|  Dallas<br>San Jose<br>Washington DC | Interregionale: `us-geo`<br>Regionale: `us-south`<br>Regionale: `us-east`<br> Sito singolo: `sjc04` |
{: caption="Tabella 1. Elenca le ubicazioni di offload dei dati disponibili nelle Americhe" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Paese | Data center | Destinazioni dell'archiviazione |
|-----|-----|----|
| Germania | Francoforte | Interregionale: `eu-geo`<br>Regionale: `eu-de`  | 
| Italia | Milano | Interregionale: `eu-geo`<br> Sito singolo: `mil01`  | 
| Paesi Bassi | Amsterdam | Interregionale: `eu-geo`<br>Sito singolo: `ams03`| 
| Norvegia| Oslo | Interregionale: `eu-geo`<br> Sito singolo: `oslo1`  | 
| Regno Unito | Londra | Interregionale: `eu-geo`<br>Regionale: `eu-gb`  |
{: caption="Tabella 2. Elenca le ubicazioni di offload dei dati disponibili in Europa" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| Paese | Data center | Destinazioni dell'archiviazione |
|-----|-----|----|
| Australia | Melbourne<br>Sydney | Interregionale: `ap-geo`<br>Regionale: `au-syd`<br>Sito singolo: `mel01`  |
| Hong Kong | Hong Kong | Interregionale: `ap-geo`<br>Sito singolo: `hkg02`  |
| India | Chennai | Interregionale: `ap-geo`<br>Sito singolo: `che01` | 
| Giappone | Tokyo | Interregionale: `ap-geo`<br>Regionale: `jp-tok`  |
| Corea del Sud| Seoul | Interregionale: `ap-geo`<br>Sito singolo: `seo01`  | 
| Singapore | Singapore | Interregionale: `ap-geo`| 
{: caption="Tabella 3. Elenca le ubicazioni di offload dei dati disponibili in Asia Pacifico" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

Per ulteriori informazioni sulle destinazioni dei bucket di archiviazione, consulta la [documentazione di Cloud Object Storage](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints).
