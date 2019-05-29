---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-28"

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

# Getting started tutorial
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} helps you move terabytes to petabytes of data into {{site.data.keyword.cloud_notm}} in a fast, simple, and secure way. This tutorial shows you how to request your migration device by using the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

## Before you begin
{: #get-started-prereqs}

Before you order a {{site.data.keyword.mdms_short}} device:

- Plan your migration strategy by reviewing the [list of supported regions and cloud storage destinations](/docs/services/mass-data-migration?topic=mass-data-migration-regions).
- Ensure that you have a provisioned instance of [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} for your {{site.data.keyword.cloud_notm}} account. 
- Understand your network connection types and speeds.
- Gather your network settings, such as IP addresses and other routing details, for connecting the device to your source server.
- Identify a person who can receive, connect, and use the device at your site.

  {{site.data.keyword.mdms_short}} cannot be shipped across international borders (for example, a device cannot be ordered in one region and shipped to another region) with exception to the European Union and its 28-member countries.
  {: note}

## Creating a storage bucket
{: #get-started-create-bucket}

After you provision an instance of Cloud Object Storage, create a storage bucket to set a destination for your migrated data. 

1. From the {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of Cloud Object Storage.
2. From the _Getting started_ page, click **Create Bucket**.
3. Enter a bucket name, and select a resiliency option for your data.

   The resiliency option determines how your data is distributed by the Cloud Object Storage service across a geographic area after the data is imported into the service. {{site.data.keyword.mdms_short}} supports the _Cross Region_, _Regional_, and _Single-site_ resiliency options.  
   {: note}

4. From the list of locations, select the geographic area where you want your data to be physically stored after it's migrated into the storage bucket.

   You can transfer data only within the same country where your source data resides. This means that your Cloud Object Storage bucket destination must also be in the same country. To learn more about supported regions, see [Region availability](/docs/services/mass-data-migration?topic=mass-data-migration-regions).
   {: note}

5. From the list of storage classes, select **Standard**.
6. Click **Create bucket**.

## Requesting a device (beta)
{: #get-started-request-device}

You can request a {{site.data.keyword.mdms_short}} device by using the {{site.data.keyword.cloud_notm}} console.

Requesting a {{site.data.keyword.mdms_short}} device by using the {{site.data.keyword.cloud_notm}} console is currently a beta feature. Interested in particpating in our beta program? Check out

1. In the [{{site.data.keyword.cloud_notm}} catalog](https://{DomainName}/catalog) search bar, type _{{site.data.keyword.mdms_short}}_.
2. Click the **{{site.data.keyword.mdms_short}}** tile.
3. In the application details page, select the **Place an order** tab.
4. Start your {{site.data.keyword.mdms_short}} request by specifying the following details.

    <table>
      <tr>
        <th>Action</th>
        <th>Description</th>
      </tr>
      <tr>
        <td>Add a request name</td>
        <td>Enter an alias to identify and track your {{site.data.keyword.mdms_short}} request. Then, select the resource group that contains your provisioned instance of Cloud Object Storage.</td>
      </tr>
      <tr>
        <td>Select your Cloud Object Storage instance</td>
        <td>From the drop-down list, select your provisioned instance of Cloud Object Storage. Then, select the name that you assigned to the storage bucket where you want to store your migrated data.</td>
      </tr>
      <tr>
        <td>Add a shipping address</td>
        <td>Enter your shipping information, such as the shipping address and name of the person who will accept the delivery. From the list of countries, select the country that corresponds with the storage bucket destination that you selected in the previous step.</td>
      </tr>
      <tr>
        <td>Add your contact information</td>
        <td>Enter the name of the person who will manage data migration to your device.</td>
      </tr>
      <tr>
        <td>Configure network settings</td>
        <td>
          <p>Configure settings for the data transfer connection by entering your network configuration details.</p>
          <p>Provide the following <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">network settings</a>:</p>
          <p>
            <ul>
              <li><i>Device management settings.</i> Enter the static IP address, the netmask, and the default gateway for your remote computer.</li>
              <li><i>Data transfer settings.</i> Enter the static IP address and the netmask for the server where your source data resides.</li>
            </ul>
          </p>
        </td>
      </tr>
      <tr>
        <td>Review the order</td>
        <td>Review and confirm details about your order.</td>
      </tr>
      <caption style="caption-side:bottom;">Table 1. Describes the {{site.data.keyword.mdms_short}} request workflow</caption>
    </table>

    When you select a delivery location for your device, [consider the weight of the device](/docs/services/mass-data-migration?topic=mass-data-migration-device-specs) and accessibility. The device, along with its hard case and a foam travel case, weighs about 60 pounds. To help with transporting the device, the travel case is equipped with wheels and a pop-up handle for easy maneuvering.
    {: tip}

5. Read the {{site.data.keyword.mdms_short}} service agreement, and then select the **{{site.data.keyword.mdms_short}} Services Agreement** check box.
6. Click **Submit order** to complete your request. 

## What's next
{: #get-started-next-steps}

Success! You're all set with your {{site.data.keyword.mdms_short}} request.

- To find out more about tracking your order, check out [Managing your request](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- To find out more about receiving and connecting your device, check out [Setting up the device](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview).

