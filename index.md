---

copyright:
  years: 2017-2018
lastupdated: "2018-06-27"

---
{:new_window: target="_blank"}

# Getting Started with {{site.data.keyword.cloud_notm}} Mass Data Migration

**Prerequisites**

These are the pieces of information you need to submit a Mass Data Migration request and complete the migration.

1. Network settings for the Storage Device
   - Static IP address
   - Netmask for enabling the data transfer
2. Network settings for remote computer
   - Static IP address
   - Netmask 
   - Default Gateway to access the User Interface
3. Cloud Object Storage download destination <br/>
   **Important**: You must have at least one {{site.data.keyword.cos_full}} account, and one bucket in a US Standard Cross Region or the EU Cross Region to complete the request form. If you don't have a {{site.data.keyword.cos_full_notm}}} account yet, create one before you request the Mass Data Migration device. Refer to [About {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Creating a request

1. Log in to the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} with your unique credentials.
2. Select **Storage** > **Data Migration** > **Mass Data Migration** from the Navigation Bar to access the Mass Data Migration landing page.
3. Click **Request Device** to open the order form.
4. Complete each field in the **Mass Data Migration** order form.
   - **Shipping Address** - this form is not prefilled and each field is editable. Provide the name of the person who is going to accept the device delivery in the Attention field. When you pick the delivery location, consider the weight of the device (66 lbs with its case) and accessibility. <br/> (**Note**: The device is equipped with wheels and pop-up handle for maneuvering.)
   - **Key Migration Contacts** - This form isn't prefilled. Each field is editable. More than one person can be added. 
   - **Data Center Network Configuration** - Provide network configuration details for the pre-provisioning of the Eth3 port on the Mass Data Migration device before shipment.
   - **Data Offload Destination** Select your existing target account from the list.
   - **Request Name** - Enter a name to help you track your order.
5. Select the **I have read and agree to the full terms of the Mass Data Migration Agreement** check box after you read each service agreement.
6. Click **Place Request** to submit the Request. Click **Cancel** to completely abandon the form and return to the Mass Data Migration landing page.


## Preparing and Shipping

After you submitted the request, the status for the request ticket appears as `Processing Request`. When your Request is accepted, {{site.data.keyword.IBM}} begins pre-configuring the next available device.

When the device is being prepared, the status on the [Requests](https://control.softlayer.com/storage/mdms){:new_window} page shows `Prepping Device` followed by `Awaiting Shipment`. After your Request enters `Awaiting Shipment` status, it can no longer be canceled. 

When the device is picked up by the carrier to be sent to your location, the Request status is updated to `Device Shipped`. The tracking number is shared with you in the **Order Details** section of the [Requests](https://control.softlayer.com/storage/mdms){:new_window} page.


## Receiving and Connecting

1. The device arrives pre-configured for you. Basic [powering/connectivity instruction](user-instructions.html) is included. <br/>
  **Note** - User name and storage pool password are provided separately. Check the **Request Details** in your [Requests](https://control.softlayer.com/storage/mdms){:new_window} for the credentials.
2. Point browser to the static IP address you provided in the order form.
3. Log in, enter the password to unlock the empty storage pool. <br/>
   **Note**: See the Request Details of your [Requests](https://control.softlayer.com/storage/mdms){:new_window} page for the password.
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

**Notes**

**Maintaining Uniqueness in the Bucket**

To ensure that object names are unique when they are copied into the bucket, the file path is included a prefix in the object name. For example, `/root/user/config.ini` becomes  `root/user/config.ini` when copied into the bucket.

**Buckets**

If the target bucket doesn't exist, it is created. If it does exist, it must be empty, otherwise the copy can't proceed.  

**File systems**

Symlinks and Hard links are skipped during the scan process.
