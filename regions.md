---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-24"

keywords: available storage locations

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

# Region availability
{: #regions}

With {{site.data.keyword.mdms_full}} and {{site.data.keyword.cos_full_notm}}, you can choose from different storage options to meet your availability and resiliency needs.  
{: shortdesc}

## Supported regions
{: #available-regions}

You can order a {{site.data.keyword.mdms_short}} device in the United States (US), European Union (EU), Japan, Australia, Brazil, Singapore, Hong Kong, Norway, South Korea, Canada, and Mexico.

As you plan to move data into the cloud, keep in mind the following shipping limitations:

- **{{site.data.keyword.mdms_short}} devices cannot be shipped across international borders** (excluding the European Union and its 28-member countries). For example, you cannot import data onto the device in one region, and then ship the device to another region.
- **You can transfer data only within the country where your source data resides.** This means that your Cloud Object Storage bucket destination must also be in the same country where the {{site.data.keyword.mdms_short}} device is staged for offloading data to the cloud. 

## Storage destinations
{: #storage-destinations}

Your data is migrated into Cloud Object Storage, where you can choose from different storage classes, locations, and resiliency for your stored data. 

The following tables show the storage bucket destinations that are available according to resiliency. 

| Storage destination | Data center | Availability |
|-----|-----|-----|
| US Cross Region | `us-geo`| ![Checkmark icon](../../icons/checkmark-icon.svg) |
| EU Cross Region | `eu-geo` | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| AP Cross Region | `ap-geo`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
{: caption="Table 1. Describes cross region storage availability" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table1}
{: tab-title="Cross region"}
{: tab-group="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Storage destination | Data center | Availability |
|-----|-----|-----|
| Dallas | `us-geo`| ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Washington DC | `eu-geo` | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Frankfurt | `ap-geo`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| London | `ap-geo`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Sydney | `ap-geo`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Tokyo | `ap-geo`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
{: caption="Table 2. Describes regional storage availability" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table2}
{: tab-title="Regional"}
{: tab-group="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| Storage destination | Data center | Availability |
|-----|-----|-----|
| Amsterdam, Netherlands | `ams03`| ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Chennai, India | `che01` | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Hong Kong | `hkg02`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Milan, Italy | `mil01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Melbourne, Australia| `mel01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Mexico City, Mexico| `mex01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Montréal, Canada | `mon01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Oslo, Norway| `osl01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| San Jose, USA| `sjc04`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| São Paulo, Brazil| `sao01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Seoul, South Korea| `seo01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
| Toronto, Canada | `tor01`  | ![Checkmark icon](../../icons/checkmark-icon.svg) |
{: caption="Table 3. Describes single site storage availability" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table2}
{: tab-title="Single site"}
{: tab-group="Americas"}
{: class="comparison-tab-table"}
{: row-headers}
