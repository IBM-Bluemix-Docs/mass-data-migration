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

{{site.data.keyword.mdms_short}} allows data transfers only within a single country. This means that your data source must be in the same country as the data center where the {{site.data.keyword.mdms_short}} device is staged.
{: important}

## Supported regions
{: #available-regions}

{{site.data.keyword.mdms_short}} is currently available in the United States (US), European Union (EU), Japan, Australia, Brazil, Singapore, Hong Kong, Norway, South Korea, Canada, and Mexico. Your data is migrated into Cloud Object Storage, where you can choose from different storage classes, locations, and resiliency for your stored data. 

{{site.data.keyword.mdms_short}} devices cannot be shipped across international borders (excluding the European Union and its 28-member countries). For example, a device cannot be ordered in one region and shipped to another region.
{: note}

## Storage destinations
{: #storage-destinations}

When you set a Cloud Object Storage bucket destination for your migrated data, you can choose from cross region, regional, or single-site resiliency for the following supported regions.

### Cross region storage
{: #cross-region}

{{site.data.keyword.mdms_short}} supports the following cross region storage destinations:

- US Cross Region (`us-geo`)

### Regional storage
{: #regional}

{{site.data.keyword.mdms_short}} supports the following regional storage destinations:

- Dallas (`us-south`)
- Washington DC (`us-east`)


