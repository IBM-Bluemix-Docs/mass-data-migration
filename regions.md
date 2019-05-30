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

Before you order a device, keep in mind the following shipping limitations:

- **{{site.data.keyword.mdms_short}} devices cannot be shipped across international borders** (excluding the European Union and its 28-member countries). For example, you cannot import data onto the device in one region, and then ship the device to another region.
- **You can transfer data only within the country where your source data resides.** This means that your Cloud Object Storage bucket destination must also be in the same country where the {{site.data.keyword.mdms_short}} device is staged for offloading data to the cloud. 

## Storage destinations
{: #storage-destinations}

Your data is migrated into Cloud Object Storage, where you can choose from different storage classes, locations, and resiliency for your stored data. 

{{site.data.keyword.mdms_short}} supports all storage locations and resiliency options that are available for Cloud Object Storage. For more information, see the [Cloud Object Storage documentation](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints).

