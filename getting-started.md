---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-17"

keywords:

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Getting started tutorial
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} helps you move terabytes to petabytes of data into {{site.data.keyword.cloud_notm}} in a fast, simple, and secure way. This tutorial shows you how to request your migration device by using the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

Updates in progress. We welcome your feedback! Reach out to Crystal Barragan (`@cbarragan`) on Slack, or [raise a doc issue ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.ibm.com/Bluemix-Docs/mass-data-migration/issues){: new_window} in our repository.
{: note}

## Before you begin
{: #get-started-prereqs}

To get started with {{site.data.keyword.mdms_short}}, create an {{site.data.keyword.cos_full}} instance for your {{site.data.keyword.cloud_notm}} account. Then, gather details about your network configuration.

1. [Log in to your {{site.data.keyword.cloud_notm}} account ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}){: new_window}.
2. [Create an instance of {{site.data.keyword.cos_full_notm}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/catalog/services/cloud-object-storage){: new_window}.
3. Gather the network settings that are required for enabling your data transfer connection, such as the static IP address and the netmask for the server where your source data resides.
4. Gather the network settings, such as the static IP address, the netmask, and the default gateway for your remote computer, that are required for interacting with the device's graphical user interface.

## Creating a storage bucket
{: #get-started-create-bucket}

After you create an instance of Cloud Object Storage, you're ready to designate a new storage bucket for your data. 

1. From the {{site.data.keyword.cloud_notm}} resource list, select your provisioned instance of Cloud Object Storage.
2. From the _Getting started_ page, click **Create Bucket**.
3. Enter a bucket name, and select a resiliency option for your data.

   The resiliency option determines how your data is distributed by the Cloud Object Storage service across a geographic area after the data is imported into the service. {{site.data.keyword.mdms_short}} supports the _Cross Region_ or _Regional_ resiliency options.

4. From the list of locations, select the geographic area where you want your data to be physically stored after it's migrated into the storage bucket.
5. From the list of storage classes, select **Standard**.
6. Click **Create bucket**.

## Submitting your request
{: #get-started-submit-request}

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
        <td>From the drop-down list, select your provisioned instance of Cloud Object Storage. Then, select the name that you assigned to storage bucket where you want to store your migrated data.</td>
      </tr>
      <tr>
        <td>Add a shipping address</td>
        <td>Enter your shipping information, such as shipping address and name of the person who will accept the delivery.</td>
      </tr>
      <tr>
        <td>Add your contact information</td>
        <td>Enter the name of the person who will data manage migration to your device.</td>
      </tr>
      <tr>
        <td>Configure network settings</td>
        <td>Configure settings for the data transfer connection by entering your network configuration details.</td>
      </tr>
      <tr>
        <td>Review the order</td>
        <td>Review and confirm details about your order.</td>
      </tr>
      <caption style="caption-side:bottom;">Table 1. Describes the {{site.data.keyword.mdms_short}} request options</caption>
    </table>

    When you pick a delivery location for your device, consider the weight of the device and accessibility. The device weighs 66 pounds, and it comes equipped with wheels and pop-up handle for maneuvering.
    {: tip}

5. Read the {{site.data.keyword.mdms_short}} service agreement, and then select the **{{site.data.keyword.mdms_short}} Services Agreement** check box.
6. Click **Submit order** to complete your request. 

## What's next
{: #get-started-next-steps}

Congratulations! You're all set with your {{site.data.keyword.mdms_short}} request.

- To find out more about tracking your request, check out `TBU`.
- To find out more about receiving and connecting your device, check out `TBU`.


<!--
Todo: Create new topics for each of these steps. Structure as part of the "How to" section.

## Prepare and ship
{: #get-started-prepare-ship}

After you submit the request, the status for the request ticket changes to `Processing Request`. When your Request is accepted, {{site.data.keyword.IBM}} begins pre-configuring the next available device.

When the device is being prepared, the status on the [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} page shows `Prepping Device` followed by `Awaiting Shipment`. After your request enters the `Awaiting Shipment` status, the request can no longer be canceled.

When the carrier picks up and sends the device to your location, the status for your request updates to `Device Shipped`. You can view the tracking number in the **Order Details** section of the [requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} page.


## Receive and connect
{: #get-started-receive-connect}

1. The device arrives pre-configured for you. A basic [powering and connectivity instruction](user-instructions.html) is included.

   User name and storage pool password are provided separately. Check the **Request Details** in your [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} for the credentials.
   {:note}

2. Point browser to the static IP address you provided in the order form.
3. Log in, enter the password to unlock the empty storage pool. <br/>

   See the Request Details of your [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} page for the password.
   {:tip}
4. Mount the NFS share on your server.
5. Rerun your DataShuttle inventory to ensure that any new files are captured.

## Move the data
{: #get-started-move-data}

1. Run the DataShuttle copy to move the data.
2. Lock the storage pool.
3. Gracefully shut down the Mass Data Migration device.
4. Send the box back to {{site.data.keyword.BluSoftlayer_full}} Data Center by using the shipping label that was provided.

When the device is returned to {{site.data.keyword.BluSoftlayer}} the request status changes to `Device Received`.

## Offload and access data
{: #get-started-offload-access}

During the transfer process, the request status displays as `Offloading Data`. The status changes again when the migration to the {{site.data.keyword.objectstorageshort}} Bucket is complete (`Offload Complete`). Your data is immediately accessible when the high-speed offload into your Cloud Object Storage bucket is complete.

## Erase the device
{: #get-started-erase-device}

{{site.data.keyword.IBM}} implements DOD-Level data wipe requirements to permanently erase your data from the device. When finished, your Request status displays `Erase Complete`.

-->