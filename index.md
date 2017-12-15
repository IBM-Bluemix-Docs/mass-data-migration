---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Getting Started with {{site.data.keyword.cloud_notm}} Mass Data Migration

## What You'll Need When Requesting a Device

1. Network settings for the Storage Device
   - Static IP Address
   - Netmask for enabling the data transfer
2. Network settings for remote computer
   - Static IP Address
   - Netmask 
   - Default Gateway to access the User Interface
3. Cloud Object Storage download destination <br/>
   **Important**: You must have at least one Cloud {{site.data.keyword.objectstorageshort}} account and one bucket in a US Cross Region or US South location to complete the request form. If you do not have a Cloud {{site.data.keyword.objectstorageshort}} account yet, please create one prior to requesting the Mass Data Migration device. Refer to [Getting Started with Cloud {{site.data.keyword.objectstorageshort}}](https://ibm-public-cos.github.io/crs-docs/){:new_window}.

## Step 1: Create a Request

1. Access the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Storage** > **Data Migration** > **Mass Data Migration** from the Navigation Bar to access the Mass Data Migration landing page. <br/>
![Data Transfer Service option in Customer Portal Menu](/images/DTSinControlMenu.PNG) <br/>
3. Click the **Request Device** link to open the order form.
4. Complete each field in the **Mass Data Migration** order form.
   - **Shipping Address**: this form is not prefilled and each field is editable. Please provide the name of the person who will accept the device delivery in the Attention field. When picking the delivery location, consider the weight of the device (66 lbs with its case) and accessibility. <br/> (**Note**: The device is equipped with wheels and pop-up handle for maneuvering.)
   - **Key Migration Contacts**: this form is not prefilled. Each field is editable. More than one person could be added. 
   - **Data Center Network Configuration**: provide network configuration details for the pre-provisioning of the Eth3 port on the Mass Data Migration device prior to shipment.
   - **Data Offload Destination**: select your existing target account from the drop down list.
   - **Request Name**: enter a name to help you keep track of your order.
5. Select the **I have read and agree to the full terms of the Mass Data Migration Agreement** check box after reading each service agreement provided.
6. Click **Place Request** to submit the Request. Click **Cancel** to completely abandon the form and return to the Mass Data Migration landing page.


## Step 2: Prep and Ship

After submitting the request, the status for the request ticket will appear as *Processing Request*.  When your Request has been processed, {{site.data.keyword.IBM}} will begin pre-configuring the next available device and the status on the [Requests](https://control.softlayer.com/storage/mdms){:new_window} grid will show *Prepping Device* followed by *Awaiting Shipment*.

Once the order is accepted and the device is being prepared the status on the [Requests](https://control.softlayer.com/storage/mdms){:new_window} grid shows *Prepping Device* followed by *Awaiting Shipment*. Once your Request enters *Awaiting Shipment* status, it can no longer be canceled. 

When the device is picked up by the carrier to be sent to your location, the Request status is updated to *Device Shipped*. The tracking number will be shared with you in the **Order Details** section of the [Requests](https://control.softlayer.com/storage/mdms){:new_window} grid.


## Step 3: Receive and Connect

1. The device arrives pre-configured for you. Basic [powering/connectivity instruction](user-instructions.html) will be included. <br/>
  **Note**: User name and storage pool password will be provided separately. Please check the **Request Details** in your [Requests](https://control.softlayer.com/storage/mdms){:new_window} grid for the credentials.
2. Point browser to the static IP address you provided in the order form.
3. Log in, supply password to unlock the empty storage pool. <br/>
   **Note**: See the Request Details of your [Requests](https://control.softlayer.com/storage/mdms){:new_window} grid for the password.
4. Mount the NFS share on your server.
5. Re-run your DataShuttle inventory to ensure any new files that may have been created since the application are captured.

## Step 4: Receive and Connect
1. Run the DataShuttle copy to move the data.
2. Lock the storage pool.
3. Gracefully shut down the Mass Data Migration device.
4. Ship box back to {{site.data.keyword.BluSoftlayer_full}} Data Center using provided shipping label.

When the device is returned to {{site.data.keyword.BluSoftlayer}} the request status changes to *Device Received*. 

## Step 5: Offload and Access

During the transfer process the request status displays as *Offloading Data*. The status changes again when the migration to the {{site.data.keyword.objectstorageshort}} Bucket is complete (*Offload Complete*). Your data is immediately accessible once the high-speed offload into your Cloud Object Storage bucket is complete.

## Step 6 

{{site.data.keyword.IBM}} will implement DOD-Level data wipe requirements to permanently erase your data from the device. When finished, your Request status will display *Erase Complete*.

## Additional Notes

### Uniqueness in the Bucket

To ensure object names are unique when they are copied into the bucket, the file path is included a prefix in the object name;  `/root/user/config.ini` becomes "root/user/config.ini" when copied into the bucket.

### Buckets

If the target bucket does not exist, it is created.   If it does exist, it must be empty, otherwise the copy cannot proceed.  

### File Systems

Symlinks and Hardlinks are skipped during the scan process.
