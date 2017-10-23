---

copyright:
  years: 2017
lastupdated: "2017-10-23"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Getting Started with {{site.data.keyword.cloud_notm}} Mass Data Migration

{{site.data.keyword.BluSoftlayer_full}} Mass Data Migration accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud}} using rugged, 120 TB usable capacity portable storage devices.

Using superior technology and hardware, Mass Data Migration helps overcome common data transfer challenges including high network costs, long transfer times, and security concerns – all in a single service.

## Overview of Mass Data Migration

1. Request a device to be sent to your on-prem data center and we ship a device to you overnight once the order has been processed.
2. Transfer large-scale data from your on-prem location to the device at high speeds.
3. Ship device back to us overnight with the included label, and we download your data into your {{site.data.keyword.objectstoragefull}}  bucket.


## Information to Collect Before Submitting a Request

1. Network settings for the Storage Device
   - Static IP Address
   - Netmask for enabling the data transfer
2. Network settings for remote computer
   - Static IP Address
   - Netmask 
   - Default Gateway to access the User Interface
3. Cloud Object Storage download destination <br/>
   **Important**: You must have at least one Cloud {{site.data.keyword.objectstorageshort}} account and one bucket in a US Cross Region or US South location to complete the request form. If you do not have a Cloud {{site.data.keyword.objectstorageshort}} account yet, please create one prior to requesting the MDMS Device. Refer to [Getting Started with Cloud {{site.data.keyword.objectstorageshort}}](https://ibm-public-cos.github.io/crs-docs/){:new_window}.

## Requesting a Mass Data Migration Device

1. Access the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Storage** > **Data Migration** > **Mass Data Migration** from the Navigation Bar to access the Mass Data Migration screen. <br/>
![Data Transfer Service option in Customer Portal Menu](/images/DTSinControlMenu.PNG) <br/>
3. Click **Request a device** link to open the order form.
4. Complete each field in the **Request Mass Data Migration Device** form.
   - **Shipping Address**: this form is not prefilled and each field is editable. Please provide the name of the person who will accept the device delivery in the Attention field. When picking the delivery location, consider the weight of the device (66lbs with its case) and accessibility. (Note: The device is equipped with wheels and pop-up handle for manuvering.)
   - **Key Migration Contacts**: this form is not prefilled. Each field is editable. More than one person could be added. 
   - **Data Center Network Configuration**: provide network configuration details for the pre-provisioning of the Eth3 port on the MDMS Device prior to shipment.
   - **Data Offload Destination**: select your existing target account from the drop down list.
   - **Request Name**: enter a name to help you keep track of your order.
5. Select the **I have read and agree to the entire Mass Service Agreement and Mass Data Migration Agreement** check box after reading each service agreement provided.
6. Click **Place Order** to submit the request. Click **Cancel** to cancel the action.


## What Happens Next

After submitting the request, the status for the request ticket will appear as *Processing Request*. Your order is then reviewed. If you wish to cancel your Request you may do so while the request is being processed by sending an email to mdmadmin@bg.vnet.ibm.com. 

Once the order is accepted and the device is being prepared the status of the [Active Request](https://control.softlayer.com/storage/mdms){:new_window} shows *Prepping Device* followed by *Awaiting Shipment*. Once your Request enters *Awaiting Shipment* status, it can no longer be canceled. 

When the device is sent to your location the request status is updated to *Device Shipped*. The tracking number will be shared with you in the [Active Request](https://control.softlayer.com/storage/mdms){:new_window}.

### Onboarding of Data from Your Data Center

1. The device arrives pre-configured for your data load. Basic [powering/connectivity instruction](user-instructions.html) will be included. <br/>
  **Note**: User name and storage pool password will be provided separately. Please check the Request Details of your [Active Request](https://control.softlayer.com/storage/mdms){:new_window} for the credentials.
2. Point browser to the static IP address you provided in the order form.
3. Log in, supply password to unlock the empty storage pool. <br/>
   **Note**: See the Request Details of your [Active Request](https://control.softlayer.com/storage/mdms){:new_window} for the password.
4. Mount the NFS share on your server.
5. Re-run your DataShuttle inventory to ensure any new files that may have been created since the application are captured.
6. Run the DataShuttle copy to move the data.
7. Lock the storage pool.
8. Gracefully shut down the MDMS device.
9. Ship box back to {{site.data.keyword.BluSoftlayer_full}} Data Center using provided shipping label.
10. Notify mdmsadmin@us.ibm.com the transfer is complete and device is in-flight.

When the device is returned to {{site.data.keyword.BluSoftlayer}} the request status changes to *Device Received*. During the transfer process the request status displays as *Offloading Data*. The status changes again when the migration to the {{site.data.keyword.objectstorageshort}} Bucket is complete (*Offload Complete*), and data is removed from the device (*Erase Complete*).

## Additional Notes

### Uniqueness in the Bucket

To ensure object names are unique when they are copied into the bucket, the file path is included a prefix in the object name;  `/root/user/config.ini` becomes "root/user/config.ini" when copied into the bucket.

### Buckets

If the target bucket does not exist, it is created.   If it does exist, it must be empty, otherwise the copy cannot proceed.  

### File Systems

Symlinks and Hardlinks are skipped during the scan process.
