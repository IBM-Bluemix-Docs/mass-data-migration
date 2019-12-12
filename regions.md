---

copyright:
  years: 2017, 2019
lastupdated: "2019-12-11"

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
{:preview: .preview}
{:term: .term}

# Region availability
{: #regions}

With {{site.data.keyword.mdms_full}} and {{site.data.keyword.cos_full_notm}}, you can choose from different storage options to meet your availability and resiliency needs.  
{: shortdesc}

## Supported regions
{: #available-regions}

You can order a {{site.data.keyword.mdms_short}} device in the United States (US), European Union (EU), Japan, Australia, Brazil, Singapore, Hong Kong, Norway, South Korea, Canada, and Mexico.

Before you order a device, keep in mind the following shipping and data transfer restrictions:

- **{{site.data.keyword.mdms_short}} devices cannot be shipped across international borders** (excluding the European Union). For example, you cannot import data onto the device in one region, and then ship the device to another region.
- **You can transfer data only within the country where your source data resides** (excluding the EU Cross Region and AP Cross Region). This means that your Cloud Object Storage bucket destination must also be in the same country as the data center where the {{site.data.keyword.mdms_short}} device will be staged for data offloading. 

  Effective 31 October 2019, {{site.data.keyword.mdms_short}} cannot ship devices between European Union member countries and the United Kingdom. If your company is located in the European Union, you can request a {{site.data.keyword.mdms_short}} device for use only within other European Union member countries.
  {: important}

## Storage destinations
{: #storage-destinations}

Your data is migrated into Cloud Object Storage, where you can choose from different storage classes, locations, and resiliency for your stored data. 

{{site.data.keyword.mdms_short}} supports all storage locations and resiliency options that are available for Cloud Object Storage. The following table maps each country with its available data centers and data offload options. 

The first column in the table represents the country where your company or source data is located. The second column represents the cities and associated data centers where you can receive and drop off the device. The third column lists the Cloud Object Storage bucket options that are available for offloading data.
{: tip}

| Location | Data centers | Storage destinations |
|-----|-----|----|
| Brazil | São Paulo | Single site: `sao01`  |
| Canada | Montréal<br>Toronto | Single site: `mon01` <br>Single site: `tor01` |
| Mexico| Mexico City | Single site: `mex01` |
| United States|  Dallas<br>San Jose<br>Washington DC | Cross region: `us-geo`<br>Regional: `us-south`<br>Regional: `us-east`<br>Single site: `sjc04` |
{: caption="Table 1. Lists the available data offload locations in the Americas" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Location | Data centers | Storage destinations |
|-----|-----|----|
| France | Paris | Single site: `par01` |
| Germany | Frankfurt | Cross region: `eu-geo`<br>Regional: `eu-de`  | 
| Italy | Milan | Cross region: `eu-geo`<br>Single site: `mil01`  | 
| Netherlands | Amsterdam | Cross region: `eu-geo`<br>Single site: `ams03`| 
| Norway| Oslo | Single site: `oslo1`  | 
| United Kingdom | London | Cross region: `eu-geo`<br>Regional: `eu-gb`  |
{: caption="Table 2. Lists the available data offload locations in Europe" caption-side="top"}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| Location | Data centers | Storage destinations |
|-----|-----|----|
| Australia | Melbourne<br>Sydney |  Cross region: `ap-geo`<br>Regional: `au-syd`<br>Single site: `mel01`  |
| Hong Kong SAR of the PRC | Hong Kong | Cross region: `ap-geo`<br>Single site: `hkg02`  |
| India | Chennai | Cross region: `ap-geo`<br>Single site: `che01` | 
| Japan | Tokyo | Cross region: `ap-geo`<br>Regional: `jp-tok`  |
| South Korea| Seoul | Cross region: `ap-geo`<br>Single site: `seo01`  | 
| Singapore | Singapore | Cross region: `ap-geo` | 
{: caption="Table 3. Lists the available data offload locations in Asia Pacific" caption-side="top"}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

For more information about storage bucket destinations, see the [Cloud Object Storage documentation](/docs/cloud-object-storage/basics?topic=cloud-object-storage-endpoints).