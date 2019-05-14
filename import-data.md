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

# Importing your data
{: #migrate-data}

You can move your data into a {{site.data.keyword.cos_full}} bucket by using {{site.data.keyword.mdms_full_notm}}.
{: shortdesc}

This content is currently being developed. We welcome your feedback! Reach out to Crystal Barragan (`@cbarragan`) on Slack, or [raise a doc issue ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.ibm.com/Bluemix-Docs/mass-data-migration/issues){: new_window} in our repository.
{: note}

## Accessing the user interface
{: #access-ui}

[After you configure the device for Ethernet connectivity](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-set-up-device#connect-device), you're ready to access the OSNEXUS QuantaStor user interface (UI) so you can begin loading your data onto the device.

To access the QuantaStor UI:

1. Open a web browser, and navigate to the following URL.

   ```
   https://<your_management_IP_address>
   ```
   {: codeblock}

   Replace `<your_management_IP_address>` with the IP address that is configured for your Eth1 or Eth2 network ports. Accept the certificate exception.

2. Log in to the QuantaStor UI by using the username and password that was sent to your e-mail address.

   ![Login page](/images/login.png)

   The Common Tasks wizard is displayed. Use the options from left to right to begin importing your data.

   ![Workflow icons](/images/workflow.png)

   You can reopen the Common Tasks wizard by using the **Workflow Manager** in the upper-left area of the interface.
   {:tip}

## Loading the data
{: #load-data}

The device arrives pre-configured with your IP address, user name, locked storage pool, and Network File System (NFS) share. The user password and storage pool password are communicated through a separate email.

### Step 1. Activate the storage pool
{: #activate-storage-pool}

1. In the Common Tasks wizard, click **Unlock and Start Storage Pool**.
2. Enter your storage pool passphrase, and then click **OK**.
      
   ![Activate Storage Pool](/images/StartStoragePool.png)

   When the storage pool is enabled, the NFS share is available to mount.

   By default, the share has both Network File System (NFS) and Server Message Block (SMB) protocols that are enabled with no access restrictions. You can modify access to this share for NFS or SMB by right-clicking the share name in the user inferace, and then selecting the appropriate menu option.
   {: note}

### Step 2. Mount the network share on your source server
{: #mount-network-share}

1. In the Common Tasks wizard, click **View Network Shares** to display the network shares view.
2. Close the Common Tasks wizard, and then right-click the network share name to view a list of options. 
3. Click **View Mount Command** to review mount information for the share.
4. Mount the share on your source server by using the specified commands.

   ![Mounting the share](/images/MountCommand.png)

   Be sure to specify the IP address that corresponds to the 10GbE port on the device.
   To allow for greater efficiency in data transmission, [jumbo frames ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/Jumbo_frame){:new_window} are enabled by default on the 10GbE device ports. You can change this setting for your device by using the [Modify Network Port ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://wiki.osnexus.com/index.php?title=Network_Port_Modify) option in the user interface.
   {: note}

### Step 3. Copy the data onto the network share
{: #copy-data}

1. Copy your data onto the network share. 
2. In the Common Tasks wizard, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10Gb link.
   
    ![View activity](/images/NetworkPerf.png)
3. Click **View Storage pool** to monitor storage usage and IOPS on the device.
   
    ![View Storage Pool](/images/PoolPerf.png)

## What's next
{: #import-data-next-steps}

- [Shut down the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device)
- [Return the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device)