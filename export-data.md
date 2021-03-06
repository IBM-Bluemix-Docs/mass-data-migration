---

copyright:
  years: 2021
lastupdated: "2021-03-28"

keywords: copy data from device, move data from device, export data 

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

# Copying data from the device
{: #export-data}

You can copy data from an {{site.data.keyword.mdms_full}} device by using the device user interface.

## Copying data from the device
{: #copy-data-from-device}

After you connect your server to the network share, you can start and monitor the data copy from the device.

1. Copy data from the network share by using a file copy tool that is compatible with your host computer.
2. In the Common Tasks wizard, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10Gb link.
   
    ![View activity](images/network-perf.png)
3. Click **View Storage pool** to monitor storage usage and IOPS on the device.
   
    ![View Storage Pool](images/pool-perf.png)

## Next steps
{: #export-data-next-steps}

1. [Erase your data](/docs/mass-data-migration?topic=mass-data-migration-erase-data) on the device.
2.  Gracefully [power down the device](/docs/mass-data-migration?topic=mass-data-migration-return-device#disconnect-device).
3.  Prepare the shipping label and [return the device to IBM](/docs/mass-data-migration?topic=mass-data-migration-return-device).
