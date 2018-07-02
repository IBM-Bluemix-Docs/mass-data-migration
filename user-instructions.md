---

copyright:
  years: 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# User Instructions

## Overview

The {{site.data.keyword.cloud}} Mass Migration device is a portable storage device able to present mountable Network File System (NFS) or FileNet Content Federations Services (CF)S shares and is managed through a web browser interface. The device is shipped to your data center, loaded with data onsite, then returned to an {{site.data.keyword.BluSoftlayer_full}} data center and loaded into your {{site.data.keyword.cos_full}} account.


### Power

The device ships with a C13-US power cord [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. If the device is being used outside of the United States, a power adapter may be required.

The device accepts all standard power ranges.
![Power range](/images/PowerRating.png)


### Ethernet Connectivity

There are two models of the MDMS device, one supports RJ45 only connectivity, the other supports Copper SFP+ and RJ45. 


#### RJ45 Only

![RJ45](/images/RJ45PortZoom.png)

Ports originate from the device as RJ45, and CAT6A cables are supplied. Copper SFP+ adapters are provided to convert from RJ45.  The adapters work with all switch manufacturers. These adapters are located in a pocket on the underside of the shipping lid.

- Eth1 (1 GbE-B) typically used for device management, and as such, should have a gateway specified in the IP Address configuration. This can be viewed on the LCD screen after the device is powered on (see the IP address configuration section below).  This port is used to make the web based UI available outside the data subnet.

- Eth3 (10 GbE-B) used for the data transfer and can also be used for device management. This connection should either be on the same subnet as the source data, or can be directly connected to the server if needed.

If a different form factor of ethernet connection is required, the customer must provide the converter.

NOTE: It is NOT required to configure/use Eth1 if Eth3 can be reached via a web browser.

#### Copper SFP+ and RJ45

![Copper SFP+](/images/sfp-ports-sized-port5.png)

Ports originate from the device as Coppper SFP+ and RJ45.  Both and CAT6A and Copper SFP+ cables are supplied.

- Eth5 10GbE (5) typically used for data transfer but can also be used for device management. This port runs only at 10GbE.

- Eth2 10GbE (2) typically used for device management but can also be used for data transfer. This port can run at either 1GbE or 10GbE speed. 


The data transfer connection should either be on the same subnet as the source data, or can be directly connected to the server if needed.

IP settings can be viewed/managed from the LCD screen after the device is powered on (see the IP address configuration section below).

NOTE: It is NOT required to configure/use both ports if one can be reached via a web browser.



## Step-by-step user instructions

1.	Device arrives pre-configured with your IP address, user name, locked storage pool and NFS share. The user password and storage pool password are communicated through a separate email.

2.	Determine the most appropriate place for the device to be placed; where it will reach both power and your ethernet connections and minimize foot traffic.

3.	Position the device to be connected, it can remain the transport case during use. Ensure the device is at room temperature and there's no condensation on it. Connect power using the provided power cable underneath the case lid and power on the device.<br/>
    **Note**: There are two power switches.
    ![Power switches](/images/MDMSPowerSwitch.png)
    **Note**: The device does not need to be removed from the portable case.

#### Connect RJ45 
4.	Remove the CAT6A cable from the case lid and connect it to the Eth3 (10GbE-B) port shown in the picture below.
    ![](/images/MDMSNewEth1and3.png)

5.	Connect the provided CAT6A to SFP+ adapter and connect to your 10Gb switch.

6.	If the IP address configured for Eth3 can be reached via browser HTTPS://'Your-Eth3-IPAddress', continue to the next step, otherwise connect Eth1 (1 GbE-B) port.<br/>
    **Note**: if you need to alter any IP settings for Eth3 or Eth1, see the IP address configuration section.

#### Connect Coppper SFP+
4. Remove the Copper SFP+ cable from the case lid and connect it to Eth5 10GbE (5) 
   ![](/images/sfp-ports-sized-port5.png)

5. Connect the provided Copper SFP+ cable to your 10Gb switch.

6.	If the IP address configured for Eth5 can be reached via browser HTTPS://'Your-Eth5-IPAddress', continue to the next step, otherwise connect Eth2 (10/1 GbE-B) port.<br/>
    **Note**: if you need to alter any IP settings for Eth5 or Eth2, see the IP address configuration section.


7. Open your browser and enter HTTPS://'Your-Chosen-IPAddress'. Accept the certificate exception.

8. Use the provided user name and password to log in.<br/>
    ![Login page](/images/Login.png)

9. The workflow wizard presents access to the specific items generally used in order from left to right.<br/>
    ![Workflow icons](/images/workflow.png) <br/>
    **NOTE**: The workflow can be reopened using **Workflow Manager** in the upper left of the GUI.

10.	Activate the pre-configured storage pool:
    - Click **Unlock and Start Storage Pool**.
    - Enter your Storage Pool Passphrase and click **OK**.
    ![Activate Storage Pool](/images/UnlockPool.png)

11. By default, the share has both NFS and SMB protocols enabled with no access restrictions placed on the share. To restrict access to this share (for NFS or SMB), right-click the share name and select the appropriate menu item.<br/>
    ![Restrict Share Access](/images/ShareControls.png)

12. When the storage pool is enabled, the NFS share is available to mount. In the workflow, click **View Network Shares** to see the network shares view. Close the workflow, right-click the share, and select mount command to see the share name and mount information. Mount the share on your source server and load the data. Be sure to specify the 10 GB link IP address when mounting the share.
    ![Mounting the share](/images/MountCommand.png)

13. Copy your data to the NFS share. In the workflow, click **View Network Activity** to show inbound Ethernet load in GUI as data is transferred to the device on the 10 GB link.
    ![View activity](/images/UserGuide13.png)

14. In the workflow, click **View Storage pool** to monitor storage usage and IOPS on the device.
    ![View Storage Pool](/images/UserGuide14.png)

15.	When the load is complete, gracefully power down the system. In the workflow, click **Shutdown Appliance...**.  
    ![Shutting Appliance Down](/images/Shutdown.png)

16.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their respective storage locations under the lid.

17.	Attach the provided shipping label, notify shipper, and return device to the data center for load into {{site.data.keyword.cos_full_notm}}.


## IP address configuration

The LCD screen on top of the device can be used to configure the IP addresses for the Ethernet ports. You navigate in the LCD panel using the **Up**, **Down**, **Back/ESC**, and **Forward/ENTER** buttons. **Enter** takes you into a menu and **Exit** takes you out.

When editing an IP address or subnet mask, **Enter** steps you forward one character at a time; **Exit** steps you back one character at a time. 

**Up** and **Down** toggles through the numbers for the elected location.

Use **Exit** to back up to the former menu.  

Go to **Update...** and press **Enter** to save the setting.

  ![LCD Display](/images/MDMSLCD.png)
