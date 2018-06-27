---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-27"

---
{:new_window: target="_blank"}

# {{site.data.keyword.cloud_notm}} Mass Data Migration FAQs

**What is {{site.data.keyword.cloud_notm}} Mass Data Migration?**

{{site.data.keyword.cloud}} Mass Data Migration is a physical data transfer service that accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud_notm}} by using rugged, 120 TB-usable capacity, portable storage devices. 

**How do I order a Mass Data Migration?**

Use the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} to submit your request. When your request is approved and processed, the next available device or devices are pre-configured and sent to you based on your network and shipping information. Use the following link to start now: https://control.softlayer.com/storage/mdms

**Why use Mass Data Migration?**

Mass Data Migration devices are equipped to perform in nearly any environment from data centers and offices to remote locations, warehouses, and ships. Mass Data Migration is also an alternative if over-the-network data transfer options are cost-prohibitive, too slow, or unavailable.  

**How much data can be transferred by using Mass Data Migration?**

There's virtually no limit to the amount of data you can transfer, whether it’s a few terabytes to petabytes. Each device holds up to 120 TB of usable capacity at RAID-6, but you can use multiple devices to accommodate larger workloads.

**Can multiple devices be used to move larger workloads that exceed 120 TB? If yes, how?**

Use multiple devices in parallel or in a series to move all data in a single migration or use a single device in iterative migrations. For example, transfer 1 PB of data by using nine devices in parallel, or use a single device in nine separate migrations.

**How long does it take to transfer the data?**

From the time, a customer submits a Mass Data Migration Request to when their data is accessible in their {{site.data.keyword.cos_full}} bucket, the turnaround time can be as little as seven days.  

**How long can the Mass Data Migration device be kept?** 

A device can be kept onsite at no cost for the first 10 business days. This time frame doesn’t include the day that your device is shipped or the day you receive it. If more time is needed to complete your ingestion, you can extend your use for USD 30 per day thereafter (applies to US and EU regions). 

**What network interfaces does Mass Data Migration support?** 

Mass Data Migration devices have 10 Gbps network interfaces with RJ45 (CAT6a) and SFP+ copper--RJ45 to SFP+ converter included--network ports.

**What is the Mass Data Migration default shipping option?**

Mass Data Migration uses UPS Next Day Air roundtrip delivery to ship all devices. The cost is included in the low, flat rate of USD 395 per device. Customers are unable to select alternative shipping methods currently.

**In what regions is Mass Data Migration available?**

Mass Data Migration is only available in the United States and the European Union. All data is migrated into {{site.data.keyword.cos_full}} in the US Standard Cross Region or the EU Cross Region tiers of the service. Devices can't be sent from one region and returned to another region.

**How much does it cost to import data into the {{site.data.keyword.cloud_notm}}?**

No fees are incurred for data that is transferred into the {{site.data.keyword.cloud_notm}}.

**Can Mass Data Migration be used to export data out of the {{site.data.keyword.cloud_notm}}?**

Mass Data Migration doesn't support exporting data out of the {{site.data.keyword.cloud_notm}} currently.

**Does Mass Data Migration encrypt the data?**

Mass Data Migration encrypts all data with AES 256-bit encryption and provides a strong password to unlock the storage pool. All data transfer within {{site.data.keyword.IBM}} is done over SSL.

**How does Mass Data Migration physically secure the data?**

All Mass Data Migration devices are housed in rugged and durable enclosures. These cases are waterproof, shockproof, and tamper-evident to ensure roundtrip device and data security. 

**How can the request be tracked throughout the migration process?**

To track the status of your Request, refer to the active requests section on the Mass Data Migration page in the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. You can sign in to the portal by using the following link: https://control.softlayer.com/storage/mdms

**How is data erased after it was offloaded to {{site.data.keyword.cos_full_notm}}?**

As soon as your data offload to {{site.data.keyword.cos_full}} is complete, {{site.data.keyword.IBM}} immediately initiates a four-pass DOD-level data wipe to permanently erase your data from the device. 

**What is the file interface?**

Mass Data Migration uses the Network File System (NFS).

**How is the file interface used?**

First, unlock the encryption pool. Then, mount the NFS share on the server that contains the data you intend to migrate. Begin copying your data files into the NFS share.

**What are the benefits of the file interface on Mass Data Migration?**

The file interface is based on mature file and network software that enables large numbers of large files to be copied and transported to the {{site.data.keyword.cloud_notm}}.

**How are files stored on the Mass Data Migration device?**

Mass Data Migration devices use a ZFS file system with LZ4 compression and AES 256-bit encryption.

**How much does it cost to use Mass Data Migration in the US?**

In the US, a flat rate of USD 395 is charged per device, which includes the USD 295 device fee, and USD 100 roundtrip UPS Next Day Air delivery, and 10 business days of use at your site. 

**Am I charged for {{site.data.keyword.cos_full_notm}} use?** 

The transfer of data into the {{site.data.keyword.cloud_notm}} is at no cost to you. However, standard rates apply for data that is stored in {{site.data.keyword.cos_full}} or any other {{site.data.keyword.cloud_notm}} service. You can find pricing for {{site.data.keyword.cos_full}} for the Standard Cross Region offering at the following link: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

**Can a {{site.data.keyword.cloud_notm}} Mass Data Migration device be purchased?**

{{site.data.keyword.cloud_notm}} Mass Data Migration devices are not for sale. 
