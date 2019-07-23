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

# Disponibilidad de regiones
{: #regions}

Con {{site.data.keyword.mdms_full}} y con {{site.data.keyword.cos_full_notm}}, puede elegir entre distintas opciones de almacenamiento que se ajusten a sus necesidades de disponibilidad y resiliencia.  
{: shortdesc}

## Regiones admitidas
{: #available-regions}

Puede solicitar un dispositivo {{site.data.keyword.mdms_short}} en los Estados Unidos (EE.UU.), la Unión Europea (UE), Japón, Australia, Brasil, Singapur, Hong Kong, Noruega, Corea del Sur, Canadá y México.

Antes de solicitar un dispositivo, tenga en cuenta las restricciones de envío y transferencia de datos siguientes:

- **No se pueden enviar dispositivos {{site.data.keyword.mdms_short}} entre fronteras internacionales** (excluyendo la Unión Europea y sus 28 países miembros). Por ejemplo, no puede importar datos en el dispositivo en una región y luego enviar el dispositivo a otra región.
- **Solo puede transferir datos dentro del país donde resida su origen de datos** (excluyendo regiones cruzadas de la UE y de Asia Pacífico). Esto implica que el destino del grupo de Cloud Object Storage debe estar también en el mismo país que el centro de datos donde se realizará la descarga de datos del dispositivo {{site.data.keyword.mdms_short}}. 

## Destinos de almacenamiento
{: #storage-destinations}

Los datos se migran en Cloud Object Storage, donde puede elegir entre distintas clases de almacenamiento, ubicaciones y resiliencia para los datos almacenados. 

{{site.data.keyword.mdms_short}} admite todas las opciones de ubicación de almacenamiento y resiliencia que están disponibles para Cloud Object Storage. En la tabla siguiente se correlaciona cada país con sus centros de datos y opciones de descarga de datos disponibles.

| País | Centros de datos | Destinos de almacenamiento |
|-----|-----|----|
| Brasil | São Paulo | Sitio único: `sao01`  |
| Canadá | Montreal<br>Toronto | Sitio único: `mon01` <br>Sitio único: `tor01` |
| México| Ciudad de México | Sitio único: `mex01` |
| Estados Unidos|  Dallas<br>San José<br>Washington DC | Región cruzada: `us-geo`<br>Regional: `us-south`<br>Regional: `us-east`<br>Sitio único: `sjc04` |
{: caption="Tabla 1. Muestra las ubicaciones de descarga de datos disponibles en América" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| País | Centros de datos | Destinos de almacenamiento |
|-----|-----|----|
| Alemania | Frankfurt | Región cruzada: `eu-geo`<br>Regional: `eu-de`  | 
| Italia | Milán | Región cruzada: `eu-geo`<br>Sitio único: `mil01`  | 
| Países Bajos | Amsterdam | Región cruzada: `eu-geo`<br>Sitio único: `ams03`| 
| Noruega| Oslo | Región cruzada: `eu-geo`<br>Sitio único: `oslo1`  | 
| Reino Unido | Londres | Región cruzada: `eu-geo`<br>Regional: `eu-gb`  |
{: caption="Tabla 2. Muestra las ubicaciones de descarga de datos disponibles en Europa" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| País | Centros de datos | Destinos de almacenamiento |
|-----|-----|----|
| Australia | Melbourne<br>Sídney |  Región cruzada: `ap-geo`<br>Regional: `au-syd`<br>Sitio único: `mel01`  |
| Hong Kong | Hong Kong | Región cruzada: `ap-geo`<br>Sitio único: `hkg02`  |
| India | Chennai | Región cruzada: `ap-geo`<br>Sitio único: `che01` | 
| Japón | Tokio | Región cruzada: `ap-geo`<br>Regional: `jp-tok`  |
| Corea del Sur| Seúl | Región cruzada: `ap-geo`<br>Sitio único: `seo01`  | 
| Singapur | Singapur | Región cruzada: `ap-geo` | 
{: caption="Tabla 3. Muestra las ubicaciones de descarga de datos disponibles en Asia Pacífico" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

Para obtener más información sobre los destinos de grupo de almacenamiento, consulte la
[Documentación de Cloud Object Storage](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints).
