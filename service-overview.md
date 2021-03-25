---

copyright:
  years: 2017, 2020, 2021
lastupdated: "2021-03-25"

keywords: data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# {{site.data.keyword.mdms_short}} overview
{: #overview}

You can import your data from your on-prem storage to the cloud or export your data from the cloud to your on-prem storage. {{site.data.keyword.mdms_full}} provides a portable, pre-configured storage device that is shipped to your location for easy migration of your data.
{: shortdesc}

## How it works 
{: #how-it-works}

If you request a {{site.data.keyword.mdms_short}} device to import data from your on-prem storage, IBM ships a pre-configured storage appliance to your data center. You connect the device to your network, and use the device to transfer your data. IBM uploads a copy of your data to the Cloud Object Storage bucket that you specify, and then erases data from the device. 

The following image describes the {{site.data.keyword.mdms_short}} import process.

![Describes the {{site.data.keyword.mdms_short}} import process.](images/mdms-workflow.png){: caption="Figure 1. Describes the Mass Data Migration import workflow." caption-side="bottom"}

If you request {{site.data.keyword.mdms_short}} device to export your data from the cloud to your on-prem storage, IBM copies your data from the cloud and ships a pre-configured storage appliance with your data to your data center. You connect the device to your network, and use the device to transfer your data. Once your data has been copied to your on-prem storage, you can erase the device and ship it to IBM, where it is erased again.

The following image describes the {{site.data.keyword.mdms_short}} export process.

![Describes the {{site.data.keyword.mdms_short}} export process.](images/mdms-workflow.png){: caption="Figure 2. Describes the Mass Data Migration export workflow." caption-side="bottom"}
<!--- Need Export process image from UX-Visual Designer -->

{{site.data.keyword.mdms_short}} encrypts all data with AES 256-bit encryption and provides a strong password to unlock the storage pool for each device. You can access the data only by using an assigned storage pool password, which is uniquely generated for each order. {{site.data.keyword.mdms_short}} devices are wiped securely between orders.
{: note}

You can compare your data migration options on {{site.data.keyword.cloud_notm}} by [exploring our data migration solutions](https://www.ibm.com/cloud/data-migration). To learn more about {{site.data.keyword.mdms_short}} use cases, check out the [{{site.data.keyword.mdms_short}} product page](https://www.ibm.com/cloud/mass-data-migration){: external}.
{: tip}

## Your workflow to import data
{: #your-workflow}

Ready to import your data from your on-prem storage to the cloud? Use the following checklist to transfer your data from your on-prem storage to the device.

1. [Connect the device](/docs/mass-data-migration?topic=mass-data-migration-connect-device)
2. [Update the network settings if needed](/docs/mass-data-migration?topic=mass-data-migration-ip-settings)
3. [Log in to the device user interface](/docs/mass-data-migration?topic=mass-data-migration-access-ui)
4. [Unlock the storage pool for the device](/docs/mass-data-migration?topic=mass-data-migration-unlock-storage-pool)
5. [Mount the network share](/docs/mass-data-migration?topic=mass-data-migration-connect-nfs-share)
6. [Copy data to the device](/docs/mass-data-migration?topic=mass-data-migration-copy-data)
7. [Return the device](/docs/mass-data-migration?topic=mass-data-migration-return-device)  
8. [Access your data](/docs/mass-data-migration?topic=mass-data-migration-access-data)

## Your workflow to export data
{: #your-export-workflow}

Ready to export your data from the cloud to your on-prem storage? Use the following checklist to transfer your data from the device to your on-prem storage.

1. [Connect the device](/docs/mass-data-migration?topic=mass-data-migration-connect-device)
2. [Update the network settings if needed](/docs/mass-data-migration?topic=mass-data-migration-ip-settings)
3. [Log in to the device user interface](/docs/mass-data-migration?topic=mass-data-migration-access-ui)
4. Copy your data onto the network share. 
5. View network activity and storage usage to monitor your progress.
6. Gracefully [power down the device](/docs/mass-data-migration?topic=mass-data-migration-disconnect-device).
7. Erase your data from the device. <!--- Need Erase process from Jorge -->
8. Prepare the shipping label and [return the device to IBM](/docs/mass-data-migration?topic=mass-data-migration-return-device).
9. Access the data on your on-prem storage.

## Service components
{: #components}

{{site.data.keyword.mdms_short}} comprises the following service components.

<dl>
   <dt>{{site.data.keyword.mdms_short}} dashboard</dt>
      <dd>You can create and track {{site.data.keyword.mdms_short}} orders from the service dashboard in the {{site.data.keyword.cloud_notm}} console. In the <a href="http://{DomainName}/mdms" target="_blank">{{site.data.keyword.mdms_short}} catalog page</a>, you specify your network configuration settings for the device, retrieve credentials to log in to the device, and track the status of your order. </dd>
   <dt>{{site.data.keyword.mdms_short}} device</dt>
      <dd>{{site.data.keyword.mdms_short}} provides a <a href="/docs/mass-data-migration?topic=mass-data-migration-device-overview">portable storage device</a> that is shipped to your location. The {{site.data.keyword.mdms_short}} device arrives pre-configured and ready to connect to your network.</dd>
   <dt>Device user interface</dt>
      <dd>The <a href="/docs/mass-data-migration?topic=mass-data-migration-access-ui">device user interface</a> is a local, web-based UI that you use to access the network share on the {{site.data.keyword.mdms_short}} device. The UI is based on a mature file and network software that enables large numbers of large files to be copied and transported to {{site.data.keyword.cloud_notm}}.</dd>
</dl>










