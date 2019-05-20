---

copyright:
  years:  2019
lastupdated: "2019-05-17"

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

## Copying data by using NFS
{: #copy-data-nfs}

You can copy data from your Linux-based source server onto a pre-configured storage device by using {{site.data.keyword.mdms_full}}.

The device arrives pre-configured with your IP address, user name, locked storage pool, and Network File System (NFS) share.

## Mounting the NFS share on your source server
{: #mount-nfs-share}

After you unlock and activate the storage pool, you can mount the NFS share on your source server.

To mount the network share: 

1. In the Common Tasks wizard, click **View Network Shares** to display the network shares view.
2. Close the Common Tasks wizard, and then right-click the network share name to view a list of options. 
3. Click **View Mount Command** to review mount information for the share.
4. Mount the share on your source server by using the specified commands.

   ![Mounting the share](/images/MountCommand.png)

   Be sure to specify the IP address that corresponds to the 10GbE port on the device. To allow for greater efficiency in data transmission, [jumbo frames ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/Jumbo_frame){:new_window} are enabled by default on the 10GbE device ports. You can change this setting for your device by using the [Modify Network Port ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://wiki.osnexus.com/index.php?title=Network_Port_Modify) option in the user interface.
   {: note}

## Copying data onto the network share
{: #copy-data}

Now that you're connected to the NFS share, you can start and monitor the data copy to the device.

1. Copy data onto the network share by using a file copy tool that is compatible with your host computer.

2. In the Common Tasks wizard, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10Gb link.
   
    ![View activity](/images/NetworkPerf.png)
3. Click **View Storage pool** to monitor storage usage and IOPS on the device.
   
    ![View Storage Pool](/images/PoolPerf.png)

## Next steps
{: #import-data-next-steps}

- [Disconnect the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device)
- [Ship the device to {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device)