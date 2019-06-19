---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords:

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
{:faq: data-hd-content-type='faq'}

# FAQs
{: #faqs}

## What is {{site.data.keyword.mdms_full_notm}}?
{: faq}

{{site.data.keyword.mdms_full_notm}} is a physical data transfer service that accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud_notm}} by using rugged, 120 TB-usable capacity, portable storage devices.

## How do I start using {{site.data.keyword.mdms_short}}?
{: faq}

Use the [{{site.data.keyword.cloud_notm}} infrastructure portal](https://control.softlayer.com/){: external} to submit your request. When your request is approved and processed, the next available device or devices are configured and sent to you based on your network and shipping information. 

## Who should use {{site.data.keyword.mdms_short}}?
{: faq}

From data centers and offices to remote locations like oil rigs and ships, {{site.data.keyword.mdms_short}} devices are equipped to perform in nearly any environment. {{site.data.keyword.mdms_short}} is also a great alternative if over-the-network data transfer options are too cost-prohibitive, slow, or unavailable.


## How much data can I transfer by using {{site.data.keyword.mdms_short}}?
{: faq}

There is virtually no limit to the amount of data you can transfer, whether it’s a few terabytes or many petabytes. Each device holds up to 120 TB of usable capacity at RAID-6, but you can use multiple devices to accommodate larger workloads. {{site.data.keyword.mdms_short}} also offers inline compression, which may further increase usable capacity depending on how compressible your dataset is. The largest single object is limited to 10 TB in size.


## How do I use multiple devices to move larger workloads that exceed 120 TB?
{: faq}

Use multiple devices in parallel or in a series to move all data in a single migration or use a single device in iterative migrations. For example, transfer 1 PB of data by using nine devices in parallel, or use a single device in nine separate migrations. If you use multiple devices in parallel, keep in mind that the ingestion rate will be slower.

## How long does it take to transfer my data?
{: faq}

From the time a customer submits a {{site.data.keyword.mdms_short}} request to when their data is accessible in their IBM Cloud Object Storage bucket, the turnaround time can be a matter of days. Transfer performance can be affected by many factors like networking, bandwidth, or the number of files being transferred. For example, transferring millions of small files will take longer than the same amount of data contained in relatively fewer, larger files.

## How long can I have a {{site.data.keyword.mdms_short}} device?

A device may be kept onsite at no additional cost for the first 10 business days. This does not include the day your device is shipped, nor the day your device is returned to IBM (maximum of 2 days). If additional time is needed to complete your ingestion, you can extend your use for USD 30 per calendar day thereafter. Applies to all regions.

## What network interfaces does {{site.data.keyword.mdms_short}} support?
{: faq}

{{site.data.keyword.mdms_short}} devices have 10-Gbps network interfaces with RJ45 (CAT6a) & SFP+ copper network ports.

RJ45 to SFP+ converters are only included with device models that lack SFP+ native connections. Fiber is not supported at this time.


## What is the {{site.data.keyword.mdms_short}} default shipping option?
{: faq}

{{site.data.keyword.mdms_short}} uses UPS Next Day Air round-trip delivery to ship all devices. The cost is included in the low, flat rate of USD 395 per device. Customers are unable to select alternative shipping methods currently.


## In what regions is {{site.data.keyword.mdms_short}} available?
{: faq}

{{site.data.keyword.mdms_short}} is currently available in the United States (US), European Union (EU), Japan, Australia, Brazil, Singapore, Hong Kong, Norway, South Korea, Canada, and Mexico. Additional geographic expansion is underway. Online ordering is available in most regions. For any region without online ordering, please contact your IBM Sales Representative to inquire about using the service.

Devices cannot be shipped across international borders (for example, a device cannot be ordered in one region and shipped to another region) with exception of the European Union and its 28-member countries.
{: note}

## What is the {{site.data.keyword.mdms_short}} default shipping option in the US?
{: faq}

{{site.data.keyword.mdms_short}} uses roundtrip UPS overnight shipping for US devices. The shipping cost is included in the price. Customers are currently unable to select alternative shipping methods. 

## What is the {{site.data.keyword.mdms_short}} default shipping option in the EU?
{: faq}

{{site.data.keyword.mdms_short}} uses roundtrip FedEx overnight shipping for EU devices. The shipping cost is included in the price. Customers are currently unable to select alternative shipping methods. 

## What is the {{site.data.keyword.mdms_short}} default shipping option in all other supported regions?
{: faq}

For all supported regions outside of the US and EU, shipping vendors and shipping turnaround times will vary. The shipping cost is included in the price. Customers are currently unable to select alternative shipping methods.

In these regions, IBM is unable to book roundtrip shipping at the time of your order placement. Instead, one-way shipments are booked at the time a shipment is needed. For outbound shipments, please allow at least three business days for IBM to coordinate the shipment of your {{site.data.keyword.mdms_short}} device after you place your request.
{: note}

For non-US and non-EU orders, request a return shipment for the device at least three business days prior to the date that you want to ship the device. For example, if you want to ship the device on Friday, coordinate a return shipment on Monday of the same week. You can request a return shipment from the _Request details_ tab in the {{site.data.keyword.mdms_short}} dashboard.
{: important}

## I am located in Japan, Australia, Brazil, Canada, Mexico, Hong Kong, Singapore, Norway, or South Korea. How do I request return shipping for my {{site.data.keyword.mdms_short}} device?
{: faq}

If you are using {{site.data.keyword.mdms_short}} outside the US and EU regions, you need to request a return shipment for the device at least three business days prior to the date that you want to ship the device. For example, if you want to ship the device on Friday, coordinate a return shipment on Monday of the same week.

## How much does it cost to import data into {{site.data.keyword.cloud_notm}}?
{: faq}

No fees are incurred for data that is transferred into {{site.data.keyword.cloud_notm}}.


## Can I use {{site.data.keyword.mdms_short}} to export data out of {{site.data.keyword.cloud_notm}}?
{: faq}

{{site.data.keyword.mdms_short}} does not support exporting data out of {{site.data.keyword.cloud_notm}} at this time.


## Does {{site.data.keyword.mdms_short}} encrypt my data?
{: faq}

{{site.data.keyword.mdms_short}} encrypts all data with AES 256-bit encryption and provides a strong password to unlock the storage pool. All data transfer within {{site.data.keyword.IBM}} is done over SSL.

## How does {{site.data.keyword.mdms_short}} physically secure my data?
{: faq}

All {{site.data.keyword.mdms_short}} devices are housed in rugged and durable enclosures. These cases are waterproof, shockproof, and tamper-evident to ensure roundtrip device and data security.

## How can I track my request throughout the migration process?
{: faq}

To track the status of your request, navigate to the _Request details_ tab on the the {{site.data.keyword.mdms_short}} dashboard in the {{site.data.keyword.cloud_notm}} console.

## How do you erase my data from the {{site.data.keyword.mdms_short}} device after it is offloaded to {{site.data.keyword.cos_full_notm}}?
{: faq}

As soon as your data offload to IBM Cloud Object Storage is complete, IBM immediately erases the device using NIST data wipe standards to ensure complete erasure of all client data from devices.

## What are the file interfaces on {{site.data.keyword.mdms_short}}?
{: faq}

{{site.data.keyword.mdms_short}} supports Network File System (NFS) and Server Message Block (SMB) protocols.

## How do I use the file interface on {{site.data.keyword.mdms_short}}?
{: faq}

First, unlock the encryption pool. Then, mount the share on the server that contains the data you intend to migrate. Begin copying your data files into the network share.

## What are the benefits of the file interface on {{site.data.keyword.mdms_short}}?
{: faq}

The file interface is based on mature file and network software that enables large numbers of large files to be copied and transported to the {{site.data.keyword.cloud_notm}}.

## How are files stored on the {{site.data.keyword.mdms_short}} device?
{: faq}

{{site.data.keyword.mdms_short}} devices use a ZFS file system with LZ4 compression and AES 256-bit encryption.

## How much does it cost to use {{site.data.keyword.mdms_short}} in the US?
{: faq}

In the US, a flat rate of USD 395 is charged per device, including the USD 295 device fee, USD 100 roundtrip UPS Overnight Shipping and 10 business days of use at your site.

Your 10 days of use onsite does not include the day your device is shipped to you nor the day your device is returned to IBM (maximum of two days). If more time is needed to complete your migration beyond the allotted 10 business days, you will be charged a USD 30 per-day extension fee for each additional day of use.

## How much does it cost to use {{site.data.keyword.mdms_short}} in the EU?
{: faq}

In the EU, a flat rate of USD 445 is charged per device including the USD 295 device fee, USD 150 roundtrip FedEx Overnight shipping and 10 business days of use at your site.

Your 10 days of use onsite does not include the day your device is shipped to you nor the day your device is returned to IBM (maximum of 2 days). If more time is needed to complete your migration beyond the allotted 10 days, you will be charged a USD 30 per-day extension fee for each additional day of use.

## How much does it cost to use {{site.data.keyword.mdms_short}} in all other supported regions?
{: faq}

In all other regions (Japan, Australia, Brazil, Canada, Mexico, Hong Kong, Singapore, Norway, and South Korea), a flat rate of USD 1,145 is charged per device including the USD 295 device fee, USD 850 roundtrip shipping, and 10 business days of use at your site.

Your 10 days of use onsite does not include the day your device is shipped to you, nor the day your device is returned to IBM (a maximum of 2 days). If more time is needed to complete your migration beyond the allotted 10 days, you will be charged a USD 30 per-day extension fee for each additional day of use.

There are special shipping requirements for these regions. See above for more information.
{: note}

## Am I charged for {{site.data.keyword.cos_full_notm}} use?
{: faq}

Transferring data into {{site.data.keyword.cloud_notm}} occurs at no cost to you. However, standard rates apply for data stored in {{site.data.keyword.cos_full_notm}} or any other {{site.data.keyword.cloud_notm}} service. To learn more about pricing options in Cloud Object storage, see [{{site.data.keyword.cos_full_notm}} pricing](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}. 

## Can I buy an {{site.data.keyword.mdms_full_notm}} device?
{: faq}

{{site.data.keyword.mdms_full_notm}} devices are not available for purchase.

## How does the {{site.data.keyword.mdms_short}} process keep the uniqueness of object names?
{: faq}

To ensure that object names are unique when they are copied into a Cloud Object Storage bucket, the file path is included a prefix in the object name. For example, `/root/user/config.ini` becomes `root/user/config.ini` when it is copied into the bucket.

## What happens if the target bucket does not exist in the {{site.data.keyword.cos_full_notm}} account?
{: faq}

If the target bucket doesn't exist, it is created. If it does exist, it must be empty, otherwise the copy can't proceed.  

## Are links skipped during the scan process?
{: faq}

Yes. Symlinks and hard links are skipped during the scan process.
