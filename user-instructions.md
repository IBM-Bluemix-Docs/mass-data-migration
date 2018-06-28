---

copyright:
  years: 2018
lastupdated: "2018-06-27"

---
{:new_window: target="_blank"}

# Importing Data to the IBM Cloud Mass Migration Device

The {{site.data.keyword.cloud}} Mass Migration device is a portable storage device able to present mountable Network File System (NFS) or FileNet Content Federations Services (CFS) shares. The device is managed through a web browser interface. The device is shipped to your data center, loaded with data onsite, then returned to an {{site.data.keyword.BluSoftlayer_full}} data center and loaded into your {{site.data.keyword.cos_full}} account.


### Powering the Device

The device ships with a C13-US power cord [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. If the device is being used outside of the United States, a power adapter might be required.

The device accepts all standard power ranges.
![Power range](/images/PowerRating.png)


### Configuring Ethernet Connectivity

You need to make two ethernet connections. One connection is for device management through a browser, and the other connection is for data movement on the same subnet where the source data is located.

Both ports originate from the device as RJ45, and CAT6A cables are supplied. Copper SFP+ adapters are provided to convert from RJ45. The adapters work with all switch manufacturers. These adapters are located in a pocket on the underside of the shipping lid.

- Eth1 (1 GbE-B) is used for device management, and as such, must have a gateway that is specified in the IP address configuration. This configuration can be viewed on the LCD screen after the device is powered on (see the Configuring IP addresses section).

- Eth3 (10 GbE-B) is used for the data transfer. This connection must either be on the same subnet as the source data, or can be directly connected to the server if needed.

If a different form factor of ethernet connection is required, the customer must provide the converter.


## Loading the Data

1.	The device arrives pre-configured with your IP address, user name, locked storage pool, and NFS share. The user password and storage pool password are communicated through a separate email.

2.	Determine the most appropriate place for the device to be placed. It needs to reach both power and your ethernet (1 GbE and 10 GbE) connections, and minimize foot traffic.

3.	Position the device to be connected. Ensure that the device is at room temperature, and there's no condensation on it. Connect power by using the provided power cable underneath the case lid and power on the device.<br/>
    **Note**: Take note of the two power switches.
    ![Power switches](/images/MDMSPowerSwitch.png)
    **Note**: The device does not need to be removed from the portable case. It can remain in the transport case during use.

4.	Remove the CAT6A cable from the case lid and connect it to the Eth3 (10 GbE-B) port as shown in the picture.
    ![ETH ports](/images/MDMSNewEth1and3.png)

5.	Connect the provided CAT6A to SFP+ adapter and connect to your 10 Gb switch.

6.	If the IP address configured for Eth3 can be reached in the browser through `HTTPS://'Your-Eth3-IPAddress'`, continue to the next step. Otherwise, connect Eth1 (1 GbE-B) port.<br/>
    **Note**: if you need to alter any IP settings for Eth3 or Eth1, see the Configuring IP addresses section.

7. Open your browser, and enter `HTTPS://'Your-Eth1-IPAddress'`. Enter Eth1 for your network configuration. Accept the certificate exception.

8. Use the provided user name and password to log in.<br/>
    ![Login page](/images/Login.png)

9. The workflow wizard presents access to the specific items generally used in order from left to right.<br/>
    ![Workflow icons](/images/workflow.png) <br/>
    **NOTE**: The workflow can be reopened by using **Workflow Manager** in the upper left of the interface.

10.	Activate the pre-configured storage pool.
    - Click **Unlock and Start Storage Pool**.
    - Enter your Storage Pool Passphrase, and click **OK**.
    ![Activate Storage Pool](/images/UnlockPool.png)

11. By default, the share has both NFS and SMB protocols that are enabled with no access restrictions. To restrict access to this share (for NFS or SMB), right-click the share name, and select the appropriate menu item.<br/>
    ![Restrict Share Access](/images/ShareControls.png)

12. When the storage pool is enabled, the NFS share is available to mount. In the workflow, click **View Network Shares** to see the network shares view. Close the workflow, right-click the share, and select mount command to see the share name and mount information. Mount the share on your source server. Be sure to specify the 10 GB link IP address.
    ![Mounting the share](/images/MountCommand.png)

13. Copy your data to the NFS share. In the workflow, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10 GB link.
    ![View activity](/images/UserGuide13.png)

14. In the workflow, click **View Storage pool** to monitor storage usage and IOPS on the device.
    ![View Storage Pool](/images/UserGuide14.png)

15.	When the load is complete, gracefully power down the system. In the workflow, click **Shutdown Appliance...**.
    ![Shutting Appliance Down](/images/Shutdown.png)

16.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their storage locations under the lid.

17.	Attach the provided shipping label, notify the carrier, and return device to the data center.


## Configuring IP Addresses

The LCD screen on the device can be used to configure the IP addresses for the Ethernet ports. You move the cursor around in the LCD panel by using the **Up**, **Down**, **Back/ESC**, and **Forward/ENTER** buttons. **Enter** takes you into a menu and **Exit** takes you out.

When you edit an IP address or subnet mask, **Enter** steps you forward one character at a time; **Exit** steps you back one character at a time. 

**Up** and **Down** toggles through the numbers for the elected location.

Use **Exit** to back up to the former menu.  

Go to **Update...** and press **Enter** to save the setting.

  ![LCD Display](/images/MDMSLCD.png)
