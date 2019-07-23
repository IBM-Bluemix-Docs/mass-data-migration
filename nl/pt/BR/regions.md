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

# Disponibilidade de região
{: #regions}

Com o {{site.data.keyword.mdms_full}} e o {{site.data.keyword.cos_full_notm}}, é possível escolher entre diferentes opções de armazenamento para atender às suas necessidades de disponibilidade e resiliência.  
{: shortdesc}

## Regiões suportadas
{: #available-regions}

É possível solicitar um dispositivo {{site.data.keyword.mdms_short}} nos Estados Unidos (EUA), na União Europeia (UE), no Japão, na Austrália, no Brasil, em Cingapura, em Hong Kong, na Noruega, na Coreia do Sul, no Canadá e no México.

Antes de solicitar um dispositivo, tenha em mente as seguintes restrições de envio e transferência de dados:

- **Os dispositivos {{site.data.keyword.mdms_short}} não podem ser enviados para além de fronteiras internacionais** (exceto a União Europeia e seus 28 países-membros). Por exemplo, não é possível importar dados para um dispositivo em uma região e, em seguida, enviá-lo para outra região.
- **É possível transferir dados somente dentro do país no qual seus dados de origem estão** (exceto a região cruzada da UE e a região cruzada da Ásia-Pacífico). Isso significa que o destino de depósito do seu Cloud Object Storage também deve estar no mesmo país que o data center no qual o dispositivo {{site.data.keyword.mdms_short}} será preparado para a transferência de dados. 

## Destinos de armazenamento
{: #storage-destinations}

Seus dados são migrados para o Cloud Object Storage, no qual é possível escolher entre diferentes classes de armazenamento, locais e resiliência para seus dados armazenados. 

O {{site.data.keyword.mdms_short}} suporta todos os locais de armazenamento e opções de resiliência disponíveis para o Cloud Object Storage. A tabela a seguir mapeia cada país com seus data centers e opções de transferência de dados disponíveis.

| Country | Data centers | Destinos de armazenamento |
|-----|-----|----|
| Brasil | São Paulo | Site único: `sao01`  |
| Canadá | Montreal<br>Toronto | Site único: `mon01` <br>Site único: `tor01` |
| México| Cidade do México | Site único: `mex01` |
| Estados Unidos|  Dallas<br>São José<br>Washington DC | Região cruzada: `us-geo`<br>Regional: `us-south`<br>Regional: `us-east`<br>Site único: `sjc04` |
{: caption="Tabela 1. Lista os locais de transferência de dados disponíveis nas Américas" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Country | Data centers | Destinos de armazenamento |
|-----|-----|----|
| Alemanha | Frankfurt | Região cruzada: `eu-geo`<br>Regional: `eu-de`  | 
| Itália | Milão | Região cruzada: `eu-geo`<br>Site único: `mil01`  | 
| Países Baixos | Amsterdã | Região cruzada: `eu-geo`<br>Site único: `ams03`| 
| Noruega| Oslo | Região cruzada: `eu-geo`<br>Site único: `oslo1`  | 
| Reino Unido | Londres | Região cruzada: `eu-geo`<br>Regional: `eu-gb`  |
{: caption="Tabela 2. Lista os locais de transferência de dados disponíveis na Europa" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| Country | Data centers | Destinos de armazenamento |
|-----|-----|----|
| Austrália | Melbourne<br>Sydney |  Região cruzada: `ap-geo`<br>Regional: `au-syd`<br>Site único: `mel01`  |
| Hong Kong | Hong Kong | Região cruzada: `ap-geo`<br>Site único: `hkg02`  |
| Índia | Chennai | Região cruzada: `ap-geo`<br>Site único: `che01` | 
| Japão | Tóquio | Região cruzada: `ap-geo`<br>Regional: `jp-tok`  |
| Coreia do Sul| Seul | Região cruzada: `ap-geo`<br>Site único: `seo01`  | 
| Cingapura | Cingapura | Região cruzada: `ap-geo` | 
{: caption="Tabela 3. Lista os locais de transferência de dados disponíveis na Ásia-Pacífico" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

Para obter mais informações sobre destinos de depósito de armazenamento, consulte a [documentação do Cloud Object Storage](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints).
