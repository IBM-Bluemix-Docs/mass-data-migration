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

Start moving data from your source server into a pre-configured storage device by using {{site.data.keyword.mdms_full}.
{: shortdesc}

## Accessing the user interface
{: #access-ui}

[After you configure the {{site.data.keyword.mdms_short}} device for Ethernet connectivity](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-set-up-device#connect-device), you're ready to access the OSNEXUS QuantaStor user interface (UI) so you can begin loading your data onto the device.

### Step 1. Retrieve your service credentials
{: #retrieve-service-credentials}

To log in to the device user interface, retrieve your device credentials by navigating to the {{site.data.keyword.mdms_short}} dashboard.

1. [Log in to the {{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){: new_window}.
2. Go to **Menu** &gt; **Resource List** to view a list of your resources.
3. From your {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of {{site.data.keyword.mdms_short}}.
4. In the _Request details_ tab, navigate to the Credentials section.
5. Copy the **User name** and **Password** values.

### Step 2. Log in to the QuantaStor user interface
{: #log-in-device-ui}

To access the QuantaStor UI:

1. Open a web browser, and navigate to the static IP address that you provided in the order form.

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Replace `<device_management_IP_address>` with the IP address that is configured for your Eth1 or Eth2 network ports. Accept the certificate exception.

2. Log in to the QuantaStor UI by using the username and password that was sent to your e-mail address.

   ![Login page](/images/login.png)

   The Common Tasks wizard is displayed. Use the options from left to right to begin importing your data.

   ![Workflow icons](/images/workflow.png)

   You can reopen the Common Tasks wizard by using the **Workflow Manager** in the upper-left area of the interface.
   {:tip}

## Loading your data
{: #load-data}

The device arrives pre-configured with your IP address, user name, locked storage pool, and Network File System (NFS) share.

### Step 1. Retrieve your storage pool passphrase
{: #activate-storage-pool}

To access the storage pool on the {{site.data.keyword.mdms_short}} device, retrieve your device credentials by navigating to the {{site.data.keyword.mdms_short}} user interface.

1. [Log in to the {{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){: new_window}.
2. Go to **Menu** &gt; **Resource List** to view a list of your resources.
3. From your {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of {{site.data.keyword.mdms_short}}.
4. In the _Request details_ tab, navigate to the Credentials section.
5. Copy the **Pool lock passcode** value.

### Step 2. Activate the storage pool
{: #activate-storage-pool}

Unlock the empty storage pool by using the credentials that you retrieved in the previous step.

1. In the Common Tasks wizard, click **Unlock and Start Storage Pool**.
2. Enter the storage pool passphrase that you retrieved in step 1, and then click **OK**.
      
   ![Activate Storage Pool](/images/StartStoragePool.png)

   By default, the share has both Network File System (NFS) and Server Message Block (SMB) protocols that are enabled with no access restrictions. You can modify access to this share for NFS or SMB by right-clicking the share name in the user inferface, and then selecting the appropriate menu option.
   {: note}

### Step 3. Mount the network share on your source server
{: #mount-network-share}

After you unlock and activate the storage pool, you can mount the NFS share on your source server.

To mount the network share: 

1. In the Common Tasks wizard, click **View Network Shares** to display the network shares view.
2. Close the Common Tasks wizard, and then right-click the network share name to view a list of options. 
3. Click **View Mount Command** to review mount information for the share.
4. Mount the share on your source server by using the specified commands.

   ![Mounting the share](/images/MountCommand.png)

   Be sure to specify the IP address that corresponds to the 10GbE port on the device.
   To allow for greater efficiency in data transmission, [jumbo frames ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/Jumbo_frame){:new_window} are enabled by default on the 10GbE device ports. You can change this setting for your device by using the [Modify Network Port ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://wiki.osnexus.com/index.php?title=Network_Port_Modify) option in the user interface.
   {: note}

### Step 4. Copy data onto the network share
{: #copy-data}

After you connect to the NFS share, start and monitor the data copy.

1. Copy data onto the network share by using a file copy tool that is compatible with your host computer.

2. In the Common Tasks wizard, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10Gb link.
   
    ![View activity](/images/NetworkPerf.png)
3. Click **View Storage pool** to monitor storage usage and IOPS on the device.
   
    ![View Storage Pool](/images/PoolPerf.png)

## What's next
{: #import-data-next-steps}

- [Shut down the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device)
- [Return the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device)