---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-24"

keywords: available storage locations

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}

# Region availability
{: #regions}

With {{site.data.keyword.mdms_full}} and {{site.data.keyword.cos_full_notm}}, you can choose from different storage options to meet your availability and resiliency needs.  
{: shortdesc}

## Supported regions
{: #available-regions}

You can order a {{site.data.keyword.mdms_short}} device in the United States and the European Union. Your data is migrated into Cloud Object Storage, where you can choose from different storage classes, locations, and resiliency for your stored data. 

{{site.data.keyword.mdms_short}} devices are confined to the region where they are sent to. Devices can't be sent from one region and returned to another region.
{: note}

## Storage destinations
{: #storage-destinations}

When you set a Cloud Object Storage bucket destination for your migrated data, you can choose from cross region or regional resiliency for the following supported regions.

### Cross region storage
{: #cross-region}

{{site.data.keyword.mdms_short}} supports the following cross region storage destinations:

- US Cross Region (`us-geo`)

### Regional storage
{: #regional}

{{site.data.keyword.mdms_short}} supports the following regional storage destinations:

- Dallas (`us-south`)
- Washington DC (`us-east`)



