---

copyright:
  years: 2017, 2021
lastupdated: "2021-03-30"

keywords: how much data can I transfer, how long does it take, supported offload destinations, shipping, pricing

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
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}

# FAQs
{: #faqs}

Frequently asked questions about {{site.data.keyword.mdms_full}}.
{: shortdesc}

## What is {{site.data.keyword.mdms_full_notm}}?
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} is a physical data transfer service that accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud_notm}} by using rugged, 120 TB-usable capacity, portable storage devices. You can also use the {{site.data.keyword.mdms_short}} service to export your data from the cloud.

## How do I start using {{site.data.keyword.mdms_short}}?
{: #how-to-use-mdms}
{: faq}

Use the [{{site.data.keyword.cloud_notm}} catalog](https://{DomainName}/mdms) to submit your request. When your request is processed, the next available device or devices are configured and sent to you based on your network and shipping information.

## Who should use {{site.data.keyword.mdms_short}}?
{: #who-uses-mdms}
{: faq}

From data centers and offices to remote locations like oil rigs and ships, {{site.data.keyword.mdms_short}} devices are equipped to perform in nearly any environment. {{site.data.keyword.mdms_short}} is also a great alternative if over-the-network data transfer options are too cost-prohibitive, slow, or unavailable.

## How much data can I transfer by using {{site.data.keyword.mdms_short}}?
{: #how-much-data}
{: faq}

There is virtually no limit to the amount of data you can transfer, whether it’s a few terabytes or many petabytes. Each device holds up to 120 TB of usable capacity at RAID-6, but you can use multiple devices to accommodate larger workloads. {{site.data.keyword.mdms_short}} also offers inline compression, which may further increase usable capacity depending on how compressible your data set is. The largest single object is limited to 10 TB in size.


## How do I use multiple devices to move larger workloads that exceed 120 TB?
{: #using-multiple-devices}
{: faq}

Use multiple devices in parallel or in a series to move all data in a single migration or use a single device in iterative migrations. For example, transfer 1 PB of data by using nine devices in parallel, or use a single device in nine separate migrations. If you use multiple devices in parallel, keep in mind that the ingestion rate will be slower.

## How long does it take to transfer my data?
{: #transfer-timeline}
{: faq}

From the time a customer submits a {{site.data.keyword.mdms_short}} request to when their data is accessible in their IBM Cloud Object Storage bucket, the turnaround time can be a matter of days. Transfer performance can be affected by many factors like networking, bandwidth, or the number of files being transferred. For example, transferring millions of small files will take longer than the same amount of data contained in relatively fewer, larger files.

## How long can I have a {{site.data.keyword.mdms_short}} device?
{: #device-onsite-time}
{: support}
{: faq}

You can keep a device onsite for up to 90 days before a member of the {{site.data.keyword.mdms_short}} team will reach out to you or your IBM Client Representative. At that time, you may be asked to provide an estimated completion timeframe and/or return the device to IBM. Applies to all regions. 

## Is IBM Cloud Object Storage the only supported offload destination?
{: #supported-cloud-destination}
{: support}
{: faq}

Cloud Object Storage is currently the only supported offload destination at this time. If you need to move to move your data to a different storage solution, see [Migration guide: Moving data from Cloud Object Storage to File or Block Storage](/docs/mass-data-migration?topic=mass-data-migration-move-data-from-cos).

## What network interfaces does {{site.data.keyword.mdms_short}} support?
{: #supported-network-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} devices have 10-Gbps network interfaces with RJ45 (CAT6a) & SFP+ copper network ports.

RJ45 to SFP+ converters are only included with device models that lack SFP+ native connections. Fiber is not supported at this time.

## In what regions is {{site.data.keyword.mdms_short}} available?
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}} is currently available in the United States (US), European Union (EU), United Kingdom (UK), Australia, Brazil, Canada, Hong Kong SAR of the PRC, India, Japan, Mexico, Norway, Singapore, and South Korea. Online ordering is available in most regions with exception to Brazil and India. For any region without online ordering, contact your IBM Client Representative to inquire about using the service. 

Devices cannot be shipped across international borders (for example, a device cannot be ordered in one region and shipped to another region) with exception of the European Union.
{: note}

## What is the {{site.data.keyword.mdms_short}} default shipping option in the US?
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}} uses roundtrip UPS overnight shipping for US devices. The shipping cost is included in your order. Alternative shipping methods are not available at this time. 

## What is the {{site.data.keyword.mdms_short}} default shipping option in the EU, United Kingdom, and Canada?
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}} uses roundtrip FedEx overnight shipping for EU, UK, and Canada devices. The shipping cost is included in your order. Alternative shipping methods are not available at this time. 

## What is the {{site.data.keyword.mdms_short}} default shipping option in all other supported regions?
{: #default-shipping-other}
{: faq}

For all supported regions outside of the US, EU, UK, and Canada, shipping vendors and shipping turnaround times will vary. The shipping cost is included in the order. Alternative shipping methods are not available at this time. 

In these regions, IBM is unable to book roundtrip shipping at the time of your order placement. Instead, one-way shipments are booked at the time a shipment is needed. For outbound shipments, please allow at least three business days for IBM to coordinate the shipment of your {{site.data.keyword.mdms_short}} device after your request is confirmed and processed.
{: note}

When you are finished using the device, [create a support case](https://{DomainName}/unifiedsupport/cases/manage) to request a pickup and return shipment for the device. Allow at least three business days for IBM to coordinate the device pickup. 

## I am located in Australia, Brazil, Hong Kong SAR of the PRC, India, Japan, Mexico, Norway, Singapore, or South Korea. How do I request return shipping for my {{site.data.keyword.mdms_short}} device?
{: #shipping-timetable-other}
{: faq}

If you are using {{site.data.keyword.mdms_short}} outside the US, EU, UK, and Canada regions, you need to request a return shipment for the device by [creating a support case](https://{DomainName}/unifiedsupport/cases/manage). Allow at least three business days for IBM to coordinate the device pickup.

## Does {{site.data.keyword.mdms_short}} encrypt my data?
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}} encrypts all data with AES 256-bit encryption and provides a strong password to unlock the storage pool. All data transfer within {{site.data.keyword.IBM}} is done over SSL.

## How does {{site.data.keyword.mdms_short}} physically secure my data?
{: #security}
{: faq}

All {{site.data.keyword.mdms_short}} devices are housed in rugged and durable enclosures. These cases are waterproof, and shockproof to ensure roundtrip device and data protection. Data is secured by using TPM. See [Data Security](/docs/mass-data-migration?topic=mass-data-migration-data-security) for details.

## How can I track my request throughout the migration process?
{: #how-to-track-request}
{: faq}

To track the status of your request, search for your order name in the **Services** section of your {{site.data.keyword.cloud_notm}} resource list. Click an 
order name to view order status from the {{site.data.keyword.mdms_short}} dashboard.

## How is my data erased from the {{site.data.keyword.mdms_short}} device after I have exported my data from the cloud to my on-prem storage?
{: #export-data-erasure}
{: faq}

After you copy your data from the {{site.data.keyword.mdms_short}} device to your on-prem storage, you can erase your data using the **Delete Storage Pool** feature in the device's user interface. The data is erased using the NIST 800-88 data wipe standard. As a precaution, the same procedure is repeated after a device is returned to IBM.

## How do you erase my data from the {{site.data.keyword.mdms_short}} device after it is imported to {{site.data.keyword.cos_full_notm}}?
{: #data-erasure}
{: faq}

As soon as your {{site.data.keyword.mdms_short}} order is complete, IBM immediately erases the device using the NIST 800-88 data wipe standard to ensure complete erasure of all of your data from devices.

## What are the file interfaces on {{site.data.keyword.mdms_short}}?
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} supports Network File System (NFS) and Server Message Block (SMB) protocols.

## How do I use the file interface on {{site.data.keyword.mdms_short}}?
{: #how-to-use-file-interface}
{: faq}

First, unlock the encryption pool. Then, mount the share on the server that contains the data you intend to migrate. Begin copying your data files into the network share.

## What are the benefits of the file interface on {{site.data.keyword.mdms_short}}?
{: #file-interface-benefits}
{: faq}

The file interface is based on mature file and network software that enables large numbers of large files to be copied and transported to the {{site.data.keyword.cloud_notm}}.

## How are files stored on the {{site.data.keyword.mdms_short}} device?
{: #file-storage}
{: faq}

{{site.data.keyword.mdms_short}} devices use a ZFS file system with LZ4 compression and AES 256-bit encryption.

## How much does it cost to use {{site.data.keyword.mdms_short}}?
{: #pricing-us}
{: faq}

{{site.data.keyword.mdms_short}} costs 50 USD per day to use. When importing your data to the cloud, the 50 USD daily charges begin accruing the day your Mass Data Migration device arrives at your 
location and stop accruing the day your device arrives at IBM for offload to IBM Cloud. The 50 USD pricing covers round-trip shipping. 

When exporting your data to your on-prem storage, the daily charges begin accruing when IBM starts copying your data from the cloud to the device and stop accruing when  you ship the device back to IBM.  This pricing model applies to all regions.

## Am I charged for {{site.data.keyword.cos_full_notm}} use?
{: #pricing-cos}
{: faq}

Transferring data into {{site.data.keyword.cloud_notm}} occurs at no cost to you. However, standard rates apply for data stored in {{site.data.keyword.cos_full_notm}} or any other {{site.data.keyword.cloud_notm}} service. To learn more about pricing options in Cloud Object Storage, see [{{site.data.keyword.cos_full_notm}} pricing](https://www.ibm.com/cloud/object-storage/pricing){: external}. 

## Can I buy an {{site.data.keyword.mdms_full_notm}} device?
{: #purchasing-devices}
{: faq}

{{site.data.keyword.mdms_full_notm}} devices are not available for purchase.

## How does the {{site.data.keyword.mdms_short}} process keep the uniqueness of object names?
{: #object-name-uniqueness}
{: faq}

To ensure that object names are unique when they are copied into a Cloud Object Storage bucket, the file path is included a prefix in the object name. For example, `/root/user/config.ini` becomes `root/user/config.ini` when it is copied into the bucket.

## Are links skipped during the scan process?
{: #links-scan-process}
{: faq}

Yes. Symlinks and hard links are skipped during the scan process.

## Can I connect macOS servers to {{site.data.keyword.mdms_short}} devices using SMB?
{: #connect-macOS-smb}
{: support}
{: faq}

It is possible to connect {{site.data.keyword.mdms_short}} devices to macOS servers using SMB. However, keep in mind that optimal throughput isn't attainable without significant tuning to the macOS client.

The list of tuning considerations includes and is not limited to: 

- [Disabling SMB signing on the client](/docs/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share)
- Determining a network sizing strategy
- Using TCP delayed acknowledgement (ACK)
- Enabling SMB configuration options that are specific to your implementation, data set, and network capacity

## Can I mount a NFS share with `no_root_squash` enabled?
{: #no-root-squash-option}
{: faq}

For security reasons, the `no_root_squash` option is disabled for NFS server configuration. The root user on any client host automatically gets a user identifer (UID) or group identifer (GID) that is equal to the `nfsnobody` user written to the file system. Files cannot be created on the NFS server as being owned by root.

All files written to an NFS share by a root user on a client host will have their files written to the NFS server as user `nfsnobody`.
