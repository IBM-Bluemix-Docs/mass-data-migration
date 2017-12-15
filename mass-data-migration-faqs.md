---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# {{site.data.keyword.cloud_notm}} Mass Data Migration FAQs

## Q1. What is {{site.data.keyword.cloud_notm}} Mass Data Migration? 
{{site.data.keyword.cloud}} Mass Data Migration is a physical data transfer service that accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud_notm}} using rugged, 120 TB-usable capacity, portable storage devices. 

## Q2. How do I start using Mass Data Migration? 
Use the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} to submit your request. Once your request is approved and processed, the next available device or devices will be pre-configured and shipped to you based upon your network and shipping information. Use the following link to start now: https://control.softlayer.com/storage/mdms

## Q3. Who should use Mass Data Migration? 
Mass Data Migration devices are equipped to perform in nearly any environment: from data centers and offices to remote locations, warehouses and ships. Mass Data Migration is also an alternative if over-the-network data transfer options are cost-prohibitive, too slow or unavailable.  

## Q4. How much data can I transfer using Mass Data Migration?
There is virtually no limit to the amount of data you can transfer, whether it’s a few terabytes to petabytes. Each device holds up to 120 TB of usable capacity at RAID-6, but you can use multiple devices to accommodate larger workloads.

## Q5. How do I use multiple devices to move larger workloads that exceed 120 TB? 
Use multiple devices in parallel or in a series to move all data in a single migration or use a single device in iterative migrations. For example, transfer 1 PB of data using 9 devices in parallel, or use a single device in 9 separate migrations.

## Q6. How long does it take to transfer my data? 
From the time a customer submits a Mass Data Migration Request to when their data is accessible in their {{site.data.keyword.cos_full}} bucket, the turnaround time can be as little as 7 days.  

## Q7. How long can I have a Mass Data Migration device?  
A device may be kept on-site at no cost for the first 10 business days. This does not include the day your device is shipped or the day you receive it. If additional time is needed to complete your ingestion, you can extend your use for USD 30 per day thereafter (applies to US and EU regions). 

## Q8. What network interfaces does Mass Data Migration support?  
Mass Data Migration devices have 10 Gbps network interfaces with RJ45 (CAT6a) & SFP+ copper--RJ45 to SFP+ converter included--network ports.

## Q9. What is the Mass Data Migration default shipping option? 
Mass Data Migration uses UPS Next Day Air roundtrip delivery to ship all devices. The cost is included in the low, flat rate of USD 395 per device. Customers are unable to select alternative shipping methods at this time.

## Q10. In what regions is Mass Data Migration available? 
Mass Data Migration is currently only available in the United States and the European Union. All data is migrated into {{site.data.keyword.cos_full}} in the US Standard Cross Region or the EU Cross Region tiers of the service, respectively. Devices cannot be shipped from one region and returned to another region.

## Q11: How much does it cost to import data into the {{site.data.keyword.cloud_notm}}? 
No fees are incurred for data transferred into the {{site.data.keyword.cloud_notm}}.

## Q12: Can I use Mass Data Migration to export my data out of the {{site.data.keyword.cloud_notm}}? 
Mass Data Migration does not support exporting data out of the {{site.data.keyword.cloud_notm}} at this time.

## Q13. Does Mass Data Migration encrypt my data? 
Mass Data Migration encrypts all data with AES 256-bit encryption and provides a strong password to unlock the storage pool. All data transfer within {{site.data.keyword.IBM}} is done over SSL.

## Q14. How does Mass Data Migration physically secure my data? 
All Mass Data Migration devices are housed in rugged and durable enclosures. These cases are waterproof, shockproof and tamper-evident to ensure roundtrip device and data security. 

## Q15. How can I track my request throughout the migration process? 
To track the status of your Request, refer to the active requests section on the Mass Data Migration page in the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. You can sign into the portal using the following link.

https://control.softlayer.com/storage/mdms

## Q16. How do you erase my data from the device after it has been offloaded to {{site.data.keyword.cos_full_notm}}?
As soon as your data offload to {{site.data.keyword.cos_full}} is complete, {{site.data.keyword.IBM}} immediately initiates a four-pass DOD-level data wipe to permanently erase your data from the device. 

## Q17: What is the file interface on Mass Data Migration? 
Mass Data Migration uses the Network File System (NFS).

## Q18: How do I use the file interface on Mass Data Migration? 
After you have unlocked the encryption pool, mount the NFS share on the server that contains the data you intend to migrate, then begin copying your data files into the NFS share.

## Q19: What are the benefits of the file interface on Mass Data Migration? 
The file interface is based on mature file and network software enabling large numbers of large files to be copied and transported to the {{site.data.keyword.cloud_notm}}.

## Q20: How are files stored on the Mass Data Migration device? 
Mass Data Migration devices use a ZFS file system with LZ4 compression and AES 256-bit encryption.

## Q21. How much does it cost to use Mass Data Migration in the US? 
In the US, a flat rate of USD 395 is charged per device including the USD 295 device fee, USD 100 roundtrip UPS Next Day Air delivery, and 10 business days of use at your site. 

## Q22. Am I charged for {{site.data.keyword.cos_full_notm}} use? 
The transfer of data into the {{site.data.keyword.cloud_notm}} is at no cost to you, however, standard rates will apply for data stored in {{site.data.keyword.cos_full}} or any other {{site.data.keyword.cloud_notm}} service. You can find pricing for {{site.data.keyword.cos_full}} for the Standard Cross Region offering at the following link.  

https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## Q23. Can I buy an {{site.data.keyword.cloud_notm}} Mass Data Migration device? 
{{site.data.keyword.cloud_notm}} Mass Data Migration devices are not available for purchase. 
