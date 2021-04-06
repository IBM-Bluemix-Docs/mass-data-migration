---

copyright:
  years: 2017, 2021
lastupdated: "2021-03-29"

keywords: erase data

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

# Erase data from device 
{: #erase-data}

Do the following to erase your data from the device.

1. [Log in to the device UI](/docs/mass-data-migration?topic=mass-data-migration-access-interface#access-ui) 

2. In the **Storage Management** tab, navigate to **Storage Pools --> Storage Pool --> Delete**.

   ![Storage Pool Delete](images/delete-storage-pool.png)

<p class="important" data-content: "Caution: ">When you delete a storage pool all of the storage volumes and network shares which reside in the storage pool <b>will be deleted</b>. Deletion of a storage pool includes a quick format of the devices which zeros the first 10MB of each disk. However, for secure deletion of data you must select one of the data shredding options, such as the <i>4-pass Dod 5220 22-M section 8-306 procedure</i>. The shredding is done at a block level on each disk device and is done concurrently across all disks in the storage pool.</p> 

Choosing the **Shred Data** option can significantly impact time requirements.
{: note}

3. After selecting your options, click **OK**.

<p class="important" data-content: "WARNING: ">All volumes and shares contained in the selected pool will be deleted.</p>

As a precaution, upon receiving the device back from you, IBM will erase all traces of your data using NIST 800-88 data wipe standards. This consists of a multiple-pass operation where every byte on the disk is zeroed to ensure your data is completely erased from the device and cannot be reconstructed. 
