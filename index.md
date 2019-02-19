---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="DomainName"}

# Getting Started with {{site.data.keyword.cloud_notm}} Mass Data Migration
{: # GettingStarted}

**Prerequisites**

Gather this information before you submit a Mass Data Migration request and complete the migration.

1. Network settings for the Storage Device
   - Static IP address
   - Netmask for enabling the data transfer
2. Network settings for remote computer
   - Static IP address
   - Netmask
   - Default Gateway to access the User Interface
3. Cloud Object Storage download destination <br/>

   You must have at least one {{site.data.keyword.cos_full}} account, and one bucket in a US Standard Cross Region or the EU Cross Region to complete the request form. If you don't have an {{site.data.keyword.cos_full_notm}}} account yet, create one before you request the Mass Data Migration device. Refer to [About {{site.data.keyword.cos_full}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage){:new_window}.
   {:important}

## Creating a request

1. Log in to the [IBM Cloud console](https://{DomainName}/){:new_window} and click the menu icon on the upper left. Select **Infrastructure**.

   Alternatively, you can log in to the [{{site.data.keyword.cloud_notm}} console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/catalog/){:new_window}.
2. Select **Storage** > **Data Migration** > **Mass Data Migration** from the Navigation Bar to access the Mass Data Migration landing page.
3. Click **Request Device** to open the order form.
4. Complete each field in the **Mass Data Migration** order form.
   - **Shipping address** - this form is not prefilled and each field is editable. Provide the name of the person who is going to accept the device delivery in the Attention field. When you pick the delivery location, consider the weight of the device (66 lbs with its case) and accessibility.

   The device is equipped with wheels and pop-up handle for maneuvering.
   {:note}

   - **Key migration contacts** - This form isn't prefilled. Each field is editable. More than one person can be added.
   - **Data center network configuration** - Provide network configuration details for the pre-provisioning of the Eth3 port on the Mass Data Migration device before shipment.
   - **Data offload destination** - Select your existing target account from the list.
   - **Request name** - Enter a name to help you track your order.
5. Select the **I have read and agree to the full terms of the Mass Data Migration Agreement** check box after you read each service agreement.
6. Click **Place Request** to submit the Request. Click **Cancel** to completely abandon the form and return to the Mass Data Migration landing page.


## Preparing and Shipping

After you submitted the request, the status for the request ticket appears as `Processing Request`. When your Request is accepted, {{site.data.keyword.IBM}} begins pre-configuring the next available device.

When the device is being prepared, the status on the [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} page shows `Prepping Device` followed by `Awaiting Shipment`. After your Request enters `Awaiting Shipment` status, it can no longer be canceled.

When the device is picked up by the carrier to be sent to your location, the Request status is updated to `Device Shipped`. The tracking number is shared with you in the **Order Details** section of the [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} page.


## Receiving and Connecting

1. The device arrives pre-configured for you. A basic [powering and connectivity instruction](user-instructions.html) is included. <br/>

   User name and storage pool password are provided separately. Check the **Request Details** in your [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} for the credentials.
   {:note}
2. Point browser to the static IP address you provided in the order form.
3. Log in, enter the password to unlock the empty storage pool. <br/>

   See the Request Details of your [Requests ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/storage/mdms){:new_window} page for the password.
   {:tip}
4. Mount the NFS share on your server.
5. Rerun your DataShuttle inventory to ensure that any new files are captured.

## Moving the Data
1. Run the DataShuttle copy to move the data.
2. Lock the storage pool.
3. Gracefully shut down the Mass Data Migration device.
4. Send the box back to {{site.data.keyword.BluSoftlayer_full}} Data Center by using the shipping label that was provided.

When the device is returned to {{site.data.keyword.BluSoftlayer}} the request status changes to `Device Received`.

## Offloading and Access

During the transfer process, the request status displays as `Offloading Data`. The status changes again when the migration to the {{site.data.keyword.objectstorageshort}} Bucket is complete (`Offload Complete`). Your data is immediately accessible when the high-speed offload into your Cloud Object Storage bucket is complete.

## Erasing the Device

{{site.data.keyword.IBM}} implements DOD-Level data wipe requirements to permanently erase your data from the device. When finished, your Request status displays `Erase Complete`.
