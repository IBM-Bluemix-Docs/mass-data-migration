---

copyright:
  years: 2017
lastupdated: "2017-10-04"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Getting Started with IBM Cloud Mass Data Migration

{{site.data.keyword.BluSoftlayer_full}} Mass Data Migration accelerates the secure movement of terabytes to petabytes of data into the {{site.data.keyword.cloud}} using rugged, 120 TB usable capacity portable storage devices.

Using superior technology and hardware, Mass Data Migration helps overcome common data transfer challenges including high network costs, long transfer times, and security concerns – all in a single service.

## Access the Data Transfer Service Screen

1. Access the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Storage** > **Data Migration** > **Data Transfer Service** from the Navigation Bar to access the Data Transfer Service screen. <br/>
![Data Transfer Service option in Customer Portal Menu](/images/DTSinControlMenu.PNG)

## Submit a Data Transfer Request

1. Access the **Data Transfer Service** screen in the[{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. . <br/> **Note**: This screen is only available to the master user of the account.
2. Click **Order Data Transfer Request** at the top of the screen.
3. Complete each field in the **Device Information** section according to the table below.
<table border="1"><tbody><tr><th>Field Name</th><th>Instructions</th></tr><tr><td>Device Type</td><td>The type of device being sent to the destination. If the device type is not listed, select "Other".</td></tr><tr><td>Serial Number</td><td> The serial number for the device.</td></tr><tr><td>Description</td><td>A brief description of the device. Important details to include may be identifying factors such as color, labels or stickers that are attached, etc.</td></tr><tr><td>Note</td><td>Any additional notes regarding the device or the transfer.</td></tr><tr><td>Destination</td><td>Datacenter that will receive the device.</td></tr><tr><td>Carrier</td><td>Post or express carrier used to ship the device to its destination.</td></tr><tr><td>Tracking Number</td><td>Full tracking number for the shipment.</td></tr></tbody></table>

4. Complete each field in the **Return Address** section or select the **Company Address** check box to automatically populate the fields with the company address on file.
5. Select the **Service Agreement Acknowledgement** check box after reading each service agreement provided.
6. Click **Submit Service Request** to submit the request. Click **Cancel** to cancel the action.

## What Happens Next

After submitting the request, 
## Uniqueness in the Bucket

To ensure object names are unique when they are copied into the bucket, the file path is included a prefix in the object name;  `/root/user/config.ini` becomes "root/user/config.ini" when copied into the bucket.

## Buckets

If the target bucket does not exist, it is created.   If it does exist, it must be empty, otherwise the copy cannot proceed.  

## File Systems

Symlinks and Hardlinks are skipped during the scan process.

## Onboarding of Data from Your Data Center

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
