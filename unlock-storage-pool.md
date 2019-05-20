---

copyright:
  years:  2019
lastupdated: "2019-05-14"

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

# Unlocking the storage pool
{: #unlock-storage-pool}

{{site.data.keyword.mdms_full}} devices arrive with a locked storage pool.
{: shortdesc}

Before you begin to the data ingestion process, you need to unlock and activate the storage pool for the device.

## Retrieving your storage pool passphrase
{: #retrieve-storage-pool-passcode}

To access the storage pool on the {{site.data.keyword.mdms_short}} device, retrieve your device credentials by navigating to the {{site.data.keyword.mdms_short}} request details in the {{site.data.keyword.cloud_notm}} console.

1. [Log in to the {{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){: new_window}.
2. Go to **Menu** &gt; **Resource List** to view a list of your resources.
3. From your {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of {{site.data.keyword.mdms_short}}.
4. In the _Request details_ tab, navigate to the Credentials section.
5. Copy the **Pool lock passcode** value.

## Activating the storage pool
{: #activate-storage-pool}

Unlock the empty storage pool by using the credentials that you retrieved in the previous step.

1. In the Common Tasks wizard, click **Unlock and Start Storage Pool**.
2. Enter the storage pool passphrase that you retrieved in step 1, and then click **OK**.
      
   ![Activate storage pool](/images/StartStoragePool.png)

   By default, the share has both Network File System (NFS) and Server Message Block (SMB) protocols that are enabled with no access restrictions. You can modify access to this share for NFS or SMB by right-clicking the share name in the user inferface, and then selecting the appropriate menu option.
   {: note}

## Next steps
{: #unlock-storage-pool-next-steps}

`TBU`