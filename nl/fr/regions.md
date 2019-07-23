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

# Disponibilité des régions
{: #regions}

Avec {{site.data.keyword.mdms_full}} et {{site.data.keyword.cos_full_notm}}, vous pouvez choisir entre différentes options de stockage pour répondre à vos besoins en disponibilité et en résilience.  
{: shortdesc}

## Régions prises en charge
{: #available-regions}

Vous pouvez commander un périphérique {{site.data.keyword.mdms_short}}  aux Etats-Unis, en Europe, au Japon, en Australie, au Brésil, à Singapour, à Hong Kong, en Norvège, en Corée du Sud, au Canada et au Mexique.

Avant de commander un périphérique, prenez connaissance des restrictions ci-après relatives à l'expédition et au transfert des données :

- **Les périphériques {{site.data.keyword.mdms_short}} ne peuvent pas être expédiés au-delà des frontières internationales** (à l'exception de l'Union Européenne et de ses 28 pays membre). Ainsi, vous ne pouvez pas importer des données sur le périphérique d'une région puis expédier le périphérique vers une autre région.
- **Vous ne pouvez transférer des données qu'au sein du pays dans lequel résident les données source** (à l'exception des régions Inter-région - Europe et Inter-région - Asie-Pacifique), ce qui signifie que la destination de votre compartiment Cloud Object Storage doit aussi se trouver dans le même pays que le centre de données où le périphérique {{site.data.keyword.mdms_short}} sera transféré pour le déchargement des données. 

## Destinations de stockage
{: #storage-destinations}

Vos données sont migrées dans Cloud Object Storage, où vous pouvez effectuer un choix parmi les différents emplacements et les diverses classes de stockage et options de résilience à appliquer à vos données stockées. 

{{site.data.keyword.mdms_short}} prend en charge tous les emplacements de stockage et options de résilience qui sont disponibles pour Cloud Object Storage. Le tableau suivant répertorie chaque pays, en lui associant les centres de données disponibles et les options de déchargement des données.

| Pays | Centres de données |Destinations de stockage|
|-----|-----|----|
| Brésil | São Paulo | Site unique : `sao01`  |
| Canada | Montréal<br>Toronto | Site unique : `mon01` <br>Site unique : `tor01` |
|Mexique | Mexico | Site unique : `mex01` |
| Etats-Unis|  Dallas<br>San Jose<br>Washington DC | Inter-région : `us-geo`<br>Régional : `us-south`<br>Régional : `us-east`<br>Site unique : `sjc04` |
{: caption="Tableau 1. Liste des emplacements de déchargement de données disponibles dans la région Amériques" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Pays | Centres de données |Destinations de stockage|
|-----|-----|----|
| Allemagne |Francfort | Inter-région : `eu-geo`<br>Régional : `eu-de`  | 
| Italie | Milan | Inter-région : `eu-geo`<br>Site unique : `mil01`  | 
| Pays-bas | Amsterdam | Inter-région : `eu-geo`<br>Site unique : `ams03`| 
| Norvège| Oslo | Inter-région : `eu-geo`<br>Site unique : `oslo1`  | 
| Royaume-Uni | Londres | Inter-région : `eu-geo`<br>Régional : `eu-gb`  |
{: caption="Tableau 2. Liste des emplacements de déchargement de données disponibles en Europe" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| Pays | Centres de données |Destinations de stockage|
|-----|-----|----|
| Australie | Melbourne<br>Sydney |  Inter-région : `ap-geo`<br>Régional : `au-syd`<br>Site unique : `mel01`  |
| Hong Kong | Hong Kong |  Inter-région : `ap-geo`<br>Site unique : `hkg02`  |
| Inde | Chennai |  Inter-région : `ap-geo`<br>Site unique : `che01` | 
| Japon | Tokyo |  Inter-région : `ap-geo`<br>Régional : `jp-tok`  |
|Corée du Sud | Séoul |  Inter-région : `ap-geo`<br>Site unique : `seo01`  | 
| Singapour | Singapour |  Inter-région : `ap-geo`| 
{: caption="Tableau 3. Liste des emplacements de déchargement de données disponibles dans la région Asie-Pacifique" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

Pour plus d'informations sur les destinations des compartiments de stockage, voir la [documentation Cloud Object Storage](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints).
