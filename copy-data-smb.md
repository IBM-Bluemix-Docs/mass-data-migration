---

copyright:
  years:  2019
lastupdated: "2019-05-17"

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

# Copying data by using SMB
{: #copy-data-smb}

You can copy data onto a {{site.data.keyword.mdms_full}} device by using the Server Message Block (SMB) protocol.

The device arrives pre-configured with your IP address, user name, locked storage pool, and a SMB share.

## Mounting the SMB share on your source server
{: #mount-smb-share}

After you unlock and activate the storage pool, you can mount the SMB share on your source server.

If you need to mount a SMB share on a Windows server, you can enable SMB packet signing for the device by [joining the device to Active Directory](https://blog.osnexus.com/2015/05/05/assigning-network-share-ownership-using-active-directory/){: external}. Keep in mind that SMB signing might impact network performance for your data transfer. If you do not use SMB signing in your environment, consider disabling it on the client.
{: note}

To mount the network share: 

1. In the Common Tasks wizard, click **View Network Shares** to display the network shares view.
2. Close the Common Tasks wizard, and then right-click the network share name to view a list of options. 
3. Click **View Mount Command** to review mount information for the share.
4. Mount the share on your source server by using the specified commands.

   ![Mounting the share](/images/MountCommand.png)

   Be sure to specify the IP address that corresponds to the 10GbE port on the device. To allow for greater efficiency in data transmission, [jumbo frames](https://en.wikipedia.org/wiki/Jumbo_frame){: external} are enabled by default on the 10GbE device ports. You can change this setting for your device by using the [Modify Network Port](https://wiki.osnexus.com/index.php?title=Network_Port_Modify){: external} option in the user interface.
   {: note}

## Copying data onto the network share
{: #copy-data}

Now that you're connected to the SMB share, you can start and monitor the data copy to the device.

1. Copy data onto the network share by using a file copy tool that is compatible with your host computer.

2. In the Common Tasks wizard, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10Gb link.
   
    ![View activity](/images/NetworkPerf.png)
3. Click **View Storage pool** to monitor storage usage and IOPS on the device.
   
    ![View Storage Pool](/images/PoolPerf.png)

## Next steps
{: #import-data-next-steps}

- Gracefully [power down the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device).
- Print a shipping label and [return the device to {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device).