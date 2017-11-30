---

copyright:
  years: 2017
lastupdated: "2017-09-13"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# User Instructions

## Overview

MDMS device is a portable storage device able to present mountable NFS or CFS shares and is managed via a web brower interface.  The device is shipped to a customer, loaded with data on premise, then returned to an IBM Data Center and loaded into Cloud Object Storage into the customer's account and a bucket.


### Power

The device ships with a C13-US power cord (https://en.wikipedia.org/wiki/IEC_60320).  If the device is being used outside of the United States, a power adaptor may be required.

The device accepts all standard power ranges.
![Power range](/images/PowerRating.png)


### Ethernet Connectivity

There are two ethernet connections to be made.  One for device management via a browser, and one for data movement on the same subnet where the source data resides.

Both ports originate from the device as RJ45, and CAT6A cables are supplied.  Copper SFP+ adapters are provided to convert from RJ45.  The adapters are guaranteed to work with all switch manufacturers.  These adapters are located in a pocket on the underside of the shipping lid.

Use Eth1 (a 1Gb port) is used for device management, and as such, should have a gateway specified in the IP Address configuration.  This can be viewed via the LCD after the device is powered on (see IP Address Configuration Addendum below).

Use Eth3 (a 10Gb port) for the data transfer.  This connection should either be on the same subnet as the source data, or can be direclty connected to the server if needed.

If a different form factor of ethernet connection is required, the customer must provide the converter.



## Step-by-step User Instructions

1.	Device arrives pre-configured with your IP address, Username, Locked Storage Pool and NFS Share.  The User Password and Storage Pool Password will be communicated via separate email.

2.	Determine the most appropriate place for the device to be placed; where it will reach both power and your ethernet (1GbE and 10GbE) connections and minimize foot traffic.

3.	Position the device to be connected, it can remain the transport case during use. Ensure the device is at room temperature and there is no condensation on it. Connect power using the provided power cable underneath the case lid and power on the device.<br/>
    **Note**: There are two power switches. 
    ![Power switches](/images/MDMSPowerSwitch.png) 
    **Note**: The device does not need to be removed from the portable case.
    
4.	Remove the CAT6A cable from the case lid and connect it to the Eth3 port shown in the picture below.
    ![](/images/MDMSNewEth1and3.png)
    
5.	Connect the provided CAT6A to SFP+ adapter and connect to your 10Gb switch.

6.	If the IP address configured for Eth3 can be reached via browser HTTPS://'Your-Eth3-IPAddress, continue to the next step, otherwise connect Eth1 to a 1Gb port.<br/>
    **Note**: See IP Configuration Addendum below if you need to alter any IP settings for Eth3 or Eth1.
    
7. Open your browser and enter HTTPS://'Your-Eth1-IPAddress'. Enter Eth1 as appropriate for your network configuration. Accept the certificate exception.

8.	Use the provided Username and Password to log in.<br/>
    ![Login page](/images/Login.png )
    
9.  The workflow wizard presents access to the specific items generally used in order from left to right.  <br/>
    ![Workflow icons](/images/workflow.png) <br/>
    **NOTE**: The workflow can be re-reopened using the Workflow Manager button in the upper left of the GUI. 
    
10.	Activate the pre-configured storage pool:
    - Click on **Unlock and Start Storage Pool**. 
    - Enter your Storage Pool Passphrase and click **OK**. 
    ![Activate Storage Pool](/images/UnlockPool.png)
    
11. Once the storage pool is enabled the NFS share is available to mount.  In the workflow, click **View Network Shares** to see the network shares view.  Close the workflow, right click on the share, and select mount command to  see the share name and mount information. Mount the share on your source server and load the data.
    ![](/images/MountCommand.png)
    
12. Begin to copy your data to the NFS share. In the workflow, click on **View Network Activity** to show inbound load on Eth3 from GUI as data is transferred to the device.
    ![](/images/Network.png)
    
13. In the workflow, click on **View Storage pool** to monitor storage usage on the device. 
    ![](/images/StoragePool.png) 
    
14.	When the load is complete, gracefully power down the system. In the workflow, click on **Shutdown Appliance...**.  
    ![](/images/Shutdown.png)
    
15.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their respective storage locations under the lid.

16.	Attach the provided shipping label, notify shipper, and return device to the data center for load into Cloud Object Storage.

## IP Address Configuration Addendum
The LCD panel on top of the device can be used to configure the IP addresses for the Ethernet ports.
You navigate in the LCD panel using the Up, Down, Back/Esc, and Forward/Enter buttons. Enter takes you into a menu and Exit takes you out.

When editing an IP address or subnet mask, Enter steps you forward one character at a time; Exit steps you back one character at a time. Up and Down toggles through the numbers for the elected location.
Use Exit back up to the former menu.  

Navigate Down to the “Update...” menu item and press Enter to save the setting.

  ![](/images/MDMSLCD.png)

