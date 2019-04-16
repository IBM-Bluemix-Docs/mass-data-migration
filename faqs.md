---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-16"

keywords:

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
{:faq: data-hd-content-type='faq'}

# FAQs
{: #faqs}

## What is {{site.data.keyword.mdms_full_notm}}?
{: faq}

{{site.data.keyword.mdms_full_notm}} is a physical data transfer service that accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud_notm}} by using rugged, 120 TB-usable capacity, portable storage devices.

## How is {{site.data.keyword.mdms_short}} initiated?
{: faq}

Use the [{{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/catalog/){:new_window} to submit your request. When your request is approved and processed, the next available device or devices are configured and sent to you based on your network and shipping information. Use the following link to start now: https://control.softlayer.com/storage/mdms

## Why use {{site.data.keyword.mdms_short}}?
{: faq}

{{site.data.keyword.mdms_short}} devices are equipped to perform in nearly any environment from data centers and offices to remote locations, warehouses, and ships. {{site.data.keyword.mdms_short}} is also an alternative if over-the-network data transfer options are cost-prohibitive, too slow, or unavailable.


## How much data can be transferred by using {{site.data.keyword.mdms_short}}?
{: faq}

There's virtually no limit to the amount of data you can transfer, whether it’s a few terabytes to petabytes. Each device holds up to 120 TB of usable capacity at RAID-6, but you can use multiple devices to accommodate larger workloads. The largest single object is limited to 10 TB.


## Can multiple devices be used to move larger workloads that exceed 120 TB? If yes, how?
{: faq}

Use multiple devices in parallel or in a series to move all data in a single migration or use a single device in iterative migrations. For example, transfer 1 PB of data by using nine devices in parallel, or use a single device in nine separate migrations.


## How long does it take to transfer the data?
{: faq}

From the time, a customer submits a {{site.data.keyword.mdms_short}} Request to when their data is accessible in their {{site.data.keyword.cos_full}} bucket, the turnaround time can be as little as seven days. The transfer performance is affected by the number of files to be transferred. Transferring of millions of small files take longer than the same amount of data contained in relatively few files.

## How long can the {{site.data.keyword.mdms_short}} device be kept?

A device can be kept onsite at no cost for the first 10 business days. This time frame doesn't include the day that your device is shipped or the day you receive it. If more time is needed to complete your ingestion, you can extend your use for USD 30 per day thereafter (applies to US and EU regions).

## What network interfaces does {{site.data.keyword.mdms_short}} support?
{: faq}

{{site.data.keyword.mdms_short}} devices have 10-Gbps network interfaces with RJ45 (CAT6a) and SFP+ copper network ports. The RJ45 to SFP+ converter is included. Jumbo Frames are enabled on the 10-Gbps interfaces.


## What is the {{site.data.keyword.mdms_short}} default shipping option?
{: faq}

{{site.data.keyword.mdms_short}} uses UPS Next Day Air round-trip delivery to ship all devices. The cost is included in the low, flat rate of USD 395 per device. Customers are unable to select alternative shipping methods currently.


## In what regions is {{site.data.keyword.mdms_short}} available?
{: faq}

{{site.data.keyword.mdms_short}} is only available in the United States and the European Union. All data is migrated into {{site.data.keyword.cos_full}} in the US Standard Cross Region or the EU Cross Region tiers of the service. Devices can't be sent from one region and returned to another region.


## How much does it cost to import data into the {{site.data.keyword.cloud_notm}}?
{: faq}

No fees are incurred for data that is transferred into the {{site.data.keyword.cloud_notm}}.


## Can {{site.data.keyword.mdms_short}} be used to export data out of the {{site.data.keyword.cloud_notm}}?
{: faq}

{{site.data.keyword.mdms_short}} doesn't support exporting data out of the {{site.data.keyword.cloud_notm}} currently.


## Does {{site.data.keyword.mdms_short}} encrypt the data?
{: faq}

{{site.data.keyword.mdms_short}} encrypts all data with AES 256-bit encryption and provides a strong password to unlock the storage pool. All data transfer within {{site.data.keyword.IBM}} is done over SSL.

## How does {{site.data.keyword.mdms_short}} physically secure the data?
{: faq}

All {{site.data.keyword.mdms_short}} devices are housed in rugged and durable enclosures. These cases are waterproof, shockproof, and tamper-evident to ensure roundtrip device and data security.

## How can the request be tracked throughout the migration process?
{: faq}

To track the status of your Request, refer to the active requests section on the {{site.data.keyword.mdms_short}} page in the [{{site.data.keyword.slportal}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){:new_window}. You can sign in to the portal by using the following link: https://control.softlayer.com/storage/mdms ![External link icon](../../icons/launch-glyph.svg "External link icon")

## How is data erased after it was offloaded to {{site.data.keyword.cos_full_notm}}?
{: faq}

As soon as your data offload to {{site.data.keyword.cos_full}} is complete, {{site.data.keyword.IBM}} immediately initiates a four-pass DOD-level data wipe to permanently erase your data from the device.

## What is the file interface?
{: faq}

The {{site.data.keyword.mdms_short}} device has shares with Network File System (NFS) and Server Message Block (SMB) enabled by default.

## How is the file interface used?
{: faq}

First, unlock the encryption pool. Then, mount the share on the server that contains the data you intend to migrate. Begin copying your data files into the share.

## What are the benefits of the file interface on {{site.data.keyword.mdms_short}}?
{: faq}

The file interface is based on mature file and network software that enables large numbers of large files to be copied and transported to the {{site.data.keyword.cloud_notm}}.

## How are files stored on the {{site.data.keyword.mdms_short}} device?
{: faq}

{{site.data.keyword.mdms_short}} devices use a ZFS file system with LZ4 compression and AES 256-bit encryption.

## How much does it cost to use {{site.data.keyword.mdms_short}} in the US?
{: faq}

In the US, a flat rate of USD 395 is charged per device. This cost includes the USD 295 device fee, and USD 100 round-trip UPS Next Day Air delivery, and 10 business days of use at your site.

## How much does {{site.data.keyword.cos_full_notm}} usage cost?
{: faq}

The transfer of data into the {{site.data.keyword.cloud_notm}} is at no cost to you. However, standard rates apply for data that is stored in {{site.data.keyword.cos_full}} or any other {{site.data.keyword.cloud_notm}} service. You can find pricing for {{site.data.keyword.cos_full}} for the Standard Cross Region offering at the following link: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api ![External link icon](../../icons/launch-glyph.svg "External link icon")

## Can a {{site.data.keyword.mdms_short}} device be purchased?
{: faq}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.mdms_short}} devices are not for sale.

## How does the {{site.data.keyword.mdms_short}} process keep the uniqueness of object names?
{: faq}

To ensure that object names are unique when they are copied into the bucket, the file path is included a prefix in the object name. For example, `/root/user/config.ini` becomes `root/user/config.ini` when copied into the bucket.

## What happens if the target bucket does not exist in the {{site.data.keyword.cos_full_notm}} account?
{: faq}

If the target bucket doesn't exist, it is created. If it does exist, it must be empty, otherwise the copy can't proceed.  

## Are links skipped during the scan process?
{: faq}

Yes. Symlinks and hard links are skipped during the scan process.
