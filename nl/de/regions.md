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

# Verfügbarkeit in den Regionen
{: #regions}

Mit {{site.data.keyword.mdms_full}} und {{site.data.keyword.cos_full_notm}} können Sie aus unterschiedlichen Speicheroptionen für Ihre Anforderungen hinsichtlich Verfügbarkeit und Ausfallsicherheit auswählen.   
{: shortdesc}

## Unterstützte Regionen
{: #available-regions}

Sie können eine {{site.data.keyword.mdms_short}}-Einheit in den Vereinigten Staaten (US), in der Europäischen Union (EU), in Japan, Australien, Brasilien, Singapur, Hongkong, Norwegen, Südkorea, Kanada und Mexiko bestellen. 

Bevor Sie eine Einheit bestellen, beachten Sie die folgenden Einschränkungen für den Versand und die Datenübertragung: 

- **{{site.data.keyword.mdms_short}}-Einheiten können nicht über internationale Grenzen versendet werden** (mit Ausnahme der Europäischen Union und ihrer 28 Mitgliedstaaten). Es ist beispielsweise nicht möglich, Daten in einer Region auf die Einheit zu importieren und die Einheit anschließend in eine andere Region zu senden. 
- **Sie können Daten nur innerhalb des Landes übertragen, in dem sich Ihre Quellendaten befinden** (mit Ausnahme von 'EU Cross Region' und 'AP Cross Region'). Dies bedeutet, dass Ihr Cloud Object Storage-Bucketziel sich in demselben Land befinden muss wie das Rechenzentrum, in dem die {{site.data.keyword.mdms_short}}-Einheit für die Datenauslagerung bereitgestellt wird.  

## Speicherziele
{: #storage-destinations}

Ihre Daten werden in Cloud Object Storage migriert. Dabei können Sie aus verschiedenen Speicherklassen, Standorten und Ausfallsicherheitsstufen für Ihre gespeicherten Daten wählen.  

{{site.data.keyword.mdms_short}} unterstützt alle Speicherstandorte und Ausfallsicherheitsoptionen, die für Cloud Object Storage verfügbar sind. In der folgenden Tabelle sind jedem Land die verfügbaren Rechenzentren und Datenauslagerungsoptionen zugeordnet. 

| Land | Rechenzentren | Speicherziele |
|-----|-----|----|
| Brasilien | São Paulo | Einziger Standort: `sao01`  |
| Kanada | Montréal<br>Toronto | Einziger Standort: `mon01` <br>Einziger Standort: `tor01` |
| Mexiko | Mexiko-Stadt | Einziger Standort: `mex01` |
| Vereinigte Staaten |  Dallas<br>San Jose<br>Washington DC | Cross Region: `us-geo`<br>Regional: `us-south`<br>Regional: `us-east`<br>Einziger Standort: `sjc04` |
{: caption="Tabelle 1. Liste der verfügbaren Datenauslagerungsstandorte in Nord-, Mittel- und Südamerika" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Land | Rechenzentren | Speicherziele |
|-----|-----|----|
| Deutschland | Frankfurt | Cross Region: `eu-geo`<br>Regional: `eu-de`  | 
| Italien | Mailand | Cross Region: `eu-geo`<br>Einziger Standort: `mil01`  | 
| Niederlande | Amsterdam | Cross Region: `eu-geo`<br>Einziger Standort: `ams03`| 
| Norwegen | Oslo | Cross Region: `eu-geo`<br>Einziger Standort: `oslo1`  | 
| Vereinigtes Königreich | London | Cross Region: `eu-geo`<br>Regional: `eu-gb`  |
{: caption="Tabelle 2. Liste der verfügbaren Datenauslagerungsstandorte in Europa" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| Land | Rechenzentren | Speicherziele |
|-----|-----|----|
| Australien | Melbourne<br>Sydney | Cross Region: `ap-geo`<br>Regional: `au-syd`<br>Einziger Standort: `mel01`  |
| Hongkong | Hongkong | Cross Region: `ap-geo`<br>Einziger Standort: `hkg02`  |
| Indien | Chennai | Cross Region: `ap-geo`<br>Einziger Standort: `che01` | 
| Japan | Tokio | Cross Region: `ap-geo`<br>Regional: `jp-tok`  |
| Südkorea | Seoul | Cross Region: `ap-geo`<br>Einziger Standort: `seo01`  | 
| Singapur | Singapur | Cross Region: `ap-geo` | 
{: caption="Tabelle 3. Liste der verfügbaren Datenauslagerungsstandorte in Asien/Pazifik" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

Weitere Informationen zu Speicherbucketzielen finden Sie in der [Dokumentation zu Cloud Object Storage](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints). 
