---

copyright:
  years:  2019
lastupdated: "2019-05-16"

keywords:

subcollection: mass-data-migration

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Accessing your data
{: #access-data}

You can access your migrated data by using {{site.data.keyword.cos_full}}.
{: shortdesc}

After the offload is complete, you can enjoy immediate access to your data in the cloud while {{site.data.keyword.cloud_notm}} securely wipes the device.

## Accessing your data in Cloud Object Storage
{: #access-data-cos}

When {{site.data.keyword.cloud_notm}} receives your {{site.data.keyword.mdms_short}} device, the order status in the {{site.data.keyword.mdms_short}} dashboard is updated to **Data offload**. The device is connected to the network in the {{site.data.keyword.cloud_notm}} data center, and the data copy starts automatically. 

Depending on the data size, the copy process can take from a few hours to days to complete. You can monitor the migration progress by navigating to the _Request details_ tab in the {{site.data.keyword.mdms_short}} dashboard. 

After the data copy is completed, the order status changes to **Erase data**. Your migrated data is available in the Cloud Object Storage instance that you specified when you submitted your {{site.data.keyword.mdms_short}} request. Before you delete data from your source server, verify that the data uploaded successfully to {{site.data.keyword.cloud_notm}}.

To access and verify your data: 

1. From the {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of Cloud Object Storage.
2. From the list of available storage buckets, select the bucket name that you designated for data migration.
3. Verify that the objects that are associated with the bucket correspond with the data that you copied to the {{site.data.keyword.mdms_short}} device.

## Moving data to a different storage solution
{: #move-data}

<!-- Add info from https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/ -->

`TBU`
