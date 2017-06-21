---

copyright:
  years: 2017
lastupdated: "2017-06-21"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# IBM Bluemix Mass Data Migration

Mass Data Migration accelerates the secure migration of up to 110TB of data per device into / out of Cleversafe Object Storage using physical storage appliances housed in waterproof, tamper-evident, shockproof cases.

## DataShuttle Tooling

Mass Data Migration uses the DataShuttle tool to:

- Inventory and manifest the files to be moved from the Data Center (this inventory is to be included with your application).  This tells the IBM Bluemix team how much data is to be moved so we can correctly provision an system to move the data.  
- Copy your data to the NFS share presented by the Device. Optionally you can MD5 each data item to ensure the copy is correct.
- Move your directory/file based data to Cloud Object Storage (COS) into bucket(s) you specify using your account credentials.

A link to the DataShuttle tool is included in the Order form.

## Uniqueness in the Bucket

To ensure object names are unique when they are copied into the bucket, the file path is included a prefix in the object name;  /root/user/config.ini   becomes "root/user/config.ini" when copied into the bucket.

## Buckets

If the target bucket does not exist, it is created.   If it does exist, it must be empty, otherwise the copy cannot proceed.  

## File Systems

Symlinks and Hardlinks are skipped during the scan process.

## Onboarding of Data from Your Data Center

1. The device will arrive pre-configured for your data load. Basic [powering/connectivity instruction](beta-user-instructions.html) will be included.
  **Note**: User name and storage pool password will be provided separately.
2. Point browser to the static IP address you provided in the order form.
3. Login, supply password to unlock the empty storage pool.
4. Mount the NFS share on your server.
5. Re-run your DataShuttle inventory to ensure any new files that may have been created since the application are captured.
6. Run the DataShuttle copy to move the data.
7. Lock the storage pool.
8. Gracefully shut down the MDMS device.
9. Ship box back to IBM Data Center using provided shipping label.
10. Notify mdmsadmin@us.ibm.com the transfer is complete and device is in-flight.
