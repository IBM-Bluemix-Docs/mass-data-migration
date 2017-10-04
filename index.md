---

copyright:
  years: 2017
lastupdated: "2017-10-04"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Getting Started with {{site.data.keyword.cloud_notm}} Mass Data Migration

{{site.data.keyword.BluSoftlayer_full}} Mass Data Migration accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud}} using rugged, 120 TB usable capacity portable storage devices.

Using superior technology and hardware, Mass Data Migration helps overcome common data transfer challenges including high network costs, long transfer times, and security concerns – all in a single service.

## Accessing the Mass Data Migration Screen

1. Access the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Storage** > **Data Migration** > **Mass Data Migration** from the Navigation Bar to access the Mass Data Migration screen. <br/>
![Data Transfer Service option in Customer Portal Menu](/images/DTSinControlMenu.PNG)

## Requesting a Mass Data Migration Device

1. Access the **Mass Data Migration** screen in the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. <br/><br/> **Note**: This screen is only available to the master user of the account. <br/>You must have at least one COS account and one bucket in a US Cross Region or US South location to complete the form. 
2. Click **Request a device** link to open the order form.
3. Complete each field in the **Request Mass Data Migration Device** form.
   - **Shipping Address**: this form is not prefilled. Each field is editable. 
   - **Key Migration Contacts**: this form is not prefilled. Each field is editable.
   - **Data Center Network Configuration**: provide network configuration details for the pre-provisioning of the Eth3 port on the MDMS Device prior to shipment.
   - **Data Offload Destination**: select your existing target account from the drop down list.
   - **Request Name**: enter a name to help you keep track of your order.
5. Select the **I have read and agree to the entire Mass Service Agreement and Mass Data Migration Agreement** check box after reading each service agreement provided.
6. Click **Place Order** to submit the request. Click **Cancel** to cancel the action.


## What Happens Next

After submitting the request, the status for the request ticket will appear as *Order Pending*. Once the order is accepted and the device is being prepared the status of the request shows *Shipment Pending*. When the device is sent to your location the status is updated to *Device Shipped*. When the device is returned to {{site.data.keyword.BluSoftlayer}} the ticket status changes *Device Returned*. During the transfer process the request status displays as *Migration Started*. The status changes again when the migration to the COS Bucket is complete (*Migration Complete*) and data is removed from the device (*Data Removed*).

## Additional Notes

### Uniqueness in the Bucket

To ensure object names are unique when they are copied into the bucket, the file path is included a prefix in the object name;  `/root/user/config.ini` becomes "root/user/config.ini" when copied into the bucket.

### Buckets

If the target bucket does not exist, it is created.   If it does exist, it must be empty, otherwise the copy cannot proceed.  

### File Systems

Symlinks and Hardlinks are skipped during the scan process.

### Onboarding of Data from Your Data Center

1. The device will arrive pre-configured for your data load. Basic [powering/connectivity instruction](user-instructions.html) will be included.
  **Note**: User name and storage pool password will be provided separately.
2. Point browser to the static IP address you provided in the order form.
3. Login, supply password to unlock the empty storage pool.
4. Mount the NFS share on your server.
5. Re-run your DataShuttle inventory to ensure any new files that may have been created since the application are captured.
6. Run the DataShuttle copy to move the data.
7. Lock the storage pool.
8. Gracefully shut down the MDMS device.
9. Ship box back to {{site.data.keyword.BluSoftlayer_full}} Data Center using provided shipping label.
10. Notify mdmsadmin@us.ibm.com the transfer is complete and device is in-flight.
