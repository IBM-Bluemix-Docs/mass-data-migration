---

copyright:
  years: 2017, 2019
lastupdated: "2019-12-18"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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
{:term: .term}

# Getting started tutorial
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} helps you move terabytes to petabytes of data into {{site.data.keyword.cloud_notm}} in a fast, simple, and secure way. This tutorial shows you how to request your data transfer device by using the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

For a limited time, you can order a {{site.data.keyword.mdms_short}} device free of charge, without incurring costs to your {{site.data.keyword.cloud_notm}} account. To learn more, check out [What's new](/docs/mass-data-migration?topic=mass-data-migration-releases).
{: tip}

## Before you begin
{: #get-started-prereqs}

Before you order a {{site.data.keyword.mdms_short}} device:

- Plan your migration by reviewing the [regions and locations](/docs/mass-data-migration?topic=mass-data-migration-regions) where {{site.data.keyword.mdms_short}} is available.
- Ensure that you have a provisioned instance of [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} for your {{site.data.keyword.cloud_notm}} account. 
- Understand your network connection types and speeds.
- Gather your network settings, such as IP addresses and other routing details, for connecting the device to your source server.
- Identify a person who can receive, connect, and use the device at your site.

## Step 1. Create a storage bucket
{: #get-started-create-bucket}

After you provision an instance of Cloud Object Storage, create a storage bucket to set a destination for your migrated data. 

1. [Log in to the {{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: external}.
2. From the {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of Cloud Object Storage.
3. From the _Getting started_ page, click **Create Bucket**.
4. Enter a bucket name, and select a resiliency option for your data.
   
   The resiliency option determines how your data is distributed by the Cloud Object Storage service across a geographic area after the data is imported into the service. {{site.data.keyword.mdms_short}} supports all resiliency options that are available for Cloud Object Storage.  
   {: note}
5. From the list of locations, select the geographic area where you want your data to be physically stored after it's migrated into the storage bucket.
6. From the list of storage classes, select **Standard**.
7. Click **Create bucket**.

## Step 2. Request a device
{: #get-started-request-device}

You can request a {{site.data.keyword.mdms_short}} device by using the {{site.data.keyword.cloud_notm}} console.


1. In the {{site.data.keyword.cloud_notm}} catalog, search for _Mass Data Migration_.
2. Click the **Mass Data Migration** tile to access the {{site.data.keyword.mdms_short}} order form.
3. Start your {{site.data.keyword.mdms_short}} request by specifying the following details.

    <table>
      <tr>
        <th>Action</th>
        <th>Description</th>
      </tr>
      <tr>
        <td>Add order details</td>
        <td>Enter an order alias to identify and track your {{site.data.keyword.mdms_short}} request.</td>
      </tr>
      <tr>
        <td>Add contact information</td>
        <td>Enter the name of the person who can receive and manage the device onsite.</td>
      </tr>
      <tr>
        <td>Add a shipping address</td>
        <td>
          <p>Enter your shipping information, such as the country of destination for the device and the shipping address.</p>
        </td>
      </tr>
      <tr>
        <td>Select your cloud destination</td>
        <td>From the drop-down list, select your provisioned instance of Cloud Object Storage. Then, select the name that you assigned to the storage bucket where you want to store your migrated data.</td>
      </tr>
      <tr>
        <td>Choose a configuration option</td>
        <td>
          <p>Choose from two options for configuring the device. You can pre-configure the device by entering your network configuration details.</p>
          <p>For the first option, provide the following <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">network settings</a>:</p>
          <p>
            <ul>
              <li>1Gb Device management settings. Enter the static IP address, the subnet mask, and the default gateway for your remote computer.</li>
              <li>10Gb Data transfer settings. Enter the static IP address and the subnet mask for the server where your source data resides.</li>
            </ul>
          </p>
          <p class="important" data-content: "Important: ">Choose the second option only if you're unable to provide network settings when you place the order. Keep in mind that this option requires that you <a href="/docs/mass-data-migration?topic=mass-data-migration-ip-settings#update-IP-settings">configure the device manually</a> when it arrives at your location.</p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">Table 1. Describes the {{site.data.keyword.mdms_short}} request workflow</caption>
    </table>

    When you select a delivery location for your device, consider the weight of the device and accessibility. The device, along with its hard case and a foam travel case, weighs about 60 pounds. To help with transporting the device, the travel case is equipped with wheels and a pop-up handle for easy maneuvering.
    {: tip}

4. Review your order summary, and view the {{site.data.keyword.mdms_short}} terms.
5. Click **Create** to complete your order. 

## What's next
{: #get-started-next-steps}

Success! You're all set with your {{site.data.keyword.mdms_short}} order.

A member of the {{site.data.keyword.mdms_short}} team will contact you or your IBM Client Representative to verify the request.

- To find out more about tracking your order, check out [Managing your request](/docs/mass-data-migration?topic=mass-data-migration-manage-request).
- To find out more about receiving and connecting your device, check out [Setting up the device](/docs/mass-data-migration?topic=mass-data-migration-device-overview).

