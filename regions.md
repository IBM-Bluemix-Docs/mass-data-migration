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

## Available storage destinations
{: #available-regions}

{{site.data.keyword.mdms_short}} is available in the United States and the European Union. Your data is migrated into Cloud Object Storage, where you can choose from different storage classes, locations, and resiliency for your stored data. 

{{site.data.keyword.mdms_short}} devices are confined to the region where they are sent to. Devices can't be sent from one region and returned to another region.
{: note}

## Cross-region storage
{: #cross-region}

When you set a Cloud Object Storage bucket destination for your migrated data, you can choose cross-region resiliency for the following locations:

- US Cross region (`us-geo`)

## Regional storage
{: #regional}

{{site.data.keyword.mdms_short}} supports the following regional storage destinations:

- Dallas (`us-south`)
- Washington DC (`us-east`)



