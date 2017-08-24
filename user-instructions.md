---

copyright:
  years: 2017
lastupdated: "2017-06-27"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# User Instructions


1.	Device arrives pre-configured with your IP address, Username, Locked Storage Pool and NFS Share.  The User Password and Storage Pool Password will be communicated via separate email.

2.	Determine the most appropriate place for the device to be placed; where it will reach both power and your ethernet (1GbE and 10GbE) connections and minimize foot traffic.

3.	Position the device to be connected, it can remain the transport case during use. Ensure the device is at room temperature and there is no condensation on it. Connect power using the provided power cable underneath the case lid and power on the device.<br/>
    **Note**: There are two power switches. 
    ![Power switches](/images/UserGuide2.jpg) 
    **Note**: The device does not need to be removed from the portable case.
4.	Remove the CAT6A cable from the case lid and connect it to the Eth3 port shown in the picture below.
    ![](/images/UserGuide3.jpg)
5.	Connect the provided CAT6A to SFP+ adapter and connect to your 10Gb switch.
6.	If the IP address configured for Eth3 can be reached via browser HTTPS://'Your-Eth3-IPAddress, continue to the next step, otherwise connect Eth1 to a 1Gb port.<br/>
    **Note**: See IP Configuration Addendum below if you need to alter any IP settings for Eth3 or Eth1.
7. Open your browser and enter HTTPS://'Your-Eth1-IPAddress'. Enter Eth1 as appropriate for your network configuration. Accept the certificate exception. 
    
8.	Use the provided Username and Password to log in.<br/>
    ![](/mass-data-migration/Login.png )
9.	FIX ME: Activate the pre-configured storage pool:
    - Click on **Unlock and Start Storage Pool**. 
    ![](/images/UserGuide7.png)
    - Enter your Storage Pool Password and click **OK**. 
    ![Activate Storage Pool](/images/UserGuide4.png)
10.  FIX ME: 	Once the storage pool is enabled the NFS share should be available for mounting. Click on **View Connections** to see the share name and mount information. Mount the share on your source server and load the data.<br/>
    ![](/images/UserGuide8.png)
11.  FIX ME:	Copy your data to the NFS share.  Monitor inbound load on Eth3 from GUI as data is transferred to the device. Activity on Eth3 indicates that data migration is in progress.<br/>
    ![](/images/UserGuide9.png)
12.	 FIX ME: When the load is complete, gracefully power down the system. Click on **Shutdown Appliance...**.  
    ![Right Click on Storage Systems and select Shutdown Storage System...](/images/UserGuide5.jpg)
13.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their respective storage locations under the lid.
14.	Attach the provided shipping label, notify shipper, and return device to the data center for load into Cloud Object Storage.

## IP Address Configuration Addendum
The LCD panel on top of the device can be used to configure the IP addresses for the Ethernet ports.

You navigate in the LCD panel using the **Up**, **Down**, **Back/Exit**, and **Forward/Enter** buttons. **Enter** takes you into a menu and **Exit** takes you out.

When editing an IP address or subnet mask, **Enter** steps you forward one character at a time; **Exit** steps you back one character at a time. **Up** and **Down** toggles through the numbers for the elected location.
