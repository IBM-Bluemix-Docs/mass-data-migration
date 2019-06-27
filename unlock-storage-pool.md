---

copyright:
  years:  2019
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

# Unlocking the storage pool
{: #unlock-storage-pool}

You can copy data onto the {{site.data.keyword.mdms_full}} device by first unlocking and activating the storage pool that is provisioned for the device.
{: shortdesc}

## Retrieving your storage pool passphrase (beta)
{: #retrieve-storage-pool-passcode}

To access the storage pool on the {{site.data.keyword.mdms_short}} device, retrieve your device credentials by navigating to the {{site.data.keyword.mdms_short}} request details in the {{site.data.keyword.cloud_notm}} console.

This feature is available as part of the [{{site.data.keyword.mdms_short}} beta release](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). You can also access credentials for your storage device from the _Request Details_ section in the [{{site.data.keyword.cloud_notm}} infrastructure portal](https://control.softlayer.com/storage/mdms){: external}.
{: note}

To retrieve your storage pool passphrase:

1. [Log in to the {{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: external}.
2. Go to **Menu** &gt; **Resource List** to view a list of your resources.
3. From your {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of {{site.data.keyword.mdms_short}}.
4. In the _Request details_ tab, navigate to the Credentials section.
5. Copy the **Pool lock passcode** value.

## Activating the storage pool
{: #activate-storage-pool}

Unlock the empty storage pool by using the credentials that you retrieved in the previous step.

1. [Log in to the device user interface](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. In the Common Tasks wizard, click **Unlock and Start Storage Pool**.
3. Enter the storage pool passphrase that you retrieved in step 1, and then click **OK**.
      
   ![Activate storage pool](/images/StartStoragePool.png)

   By default, the share has both Network File System (NFS) and Server Message Block (SMB) protocols that are enabled with no access restrictions. You can modify access to this share for NFS or SMB by right-clicking the share name in the user inferface, and then selecting the appropriate menu option.
   {: note}

## Next steps
{: #unlock-storage-pool-next-steps}

- If you're using a Unix machine, [connect the network share by using NFS](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share).
- If you're using a Windows machine, [connect to the network share by using SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share).
- Start the [data copy process](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy).