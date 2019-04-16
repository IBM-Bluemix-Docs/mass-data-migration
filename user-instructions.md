---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-16"

keywords:

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Importing Data to the {{site.data.keyword.mdms_full_notm}} Device
{: #userguide}

The {{site.data.keyword.mdms_full}} device is a portable storage device able to present mountable Network file system (NFS) or FileNet Content Federations Services (CFS) shares. The device is managed through a web browser interface. The device is shipped to your data center, loaded with data onsite, then returned to an {{site.data.keyword.BluSoftlayer_full}} data center and loaded into your {{site.data.keyword.cos_full}} account.
{: shortdesc}

## Powering up the Device

The device is sent with a C13-US power cord [https://en.wikipedia.org/wiki/IEC_60320 ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. If the device is used outside of the United States, a power adapter might be required.

The device accepts all standard power ranges. <br/>
![Power range](/images/PowerRating.png)

To turn on the device, complete the following steps.
1. Turn on the Mains Switch by the power plug. <br/>
   ![Mains Switch](/images/MDMSPowerOnOff.png)

2. Use the System On / Off button that is next to the connection link LEDs.
   ![System On / Off](/images/MDMSSystemOnOff.png)

The device is powered on when the System ID is shown on the LED screen.


## Configuring Ethernet Connectivity

You need to make two ethernet connections. One connection is for device management through a browser, and the other connection is for data movement on the same subnet where the source data is located.

{{site.data.keyword.cloud}} provides two models of the MDMS Device. One model supports RJ45 connectivity only. The other model supports Copper SFP+ and RJ45. Depending on the model of the MDMS device, follow the instructions that are appropriate.

By default, Jumbo Frames are enabled on 10-GbE ports. This setting can be changed by using the Modify Network Port option in the UI.
{:tip}

### Configuring RJ45 Only

![RJ45](/images/RJ45PortZoom.png)

Ports originate from the device as RJ45, and CAT6A cables are supplied. Copper SFP+ adapters are provided to convert from RJ45. The adapters work with all switch manufacturers. These adapters are located in a pocket on the underside of the shipping container lid.

- Eth1 (`1GbE-B`) is typically used for device management, and as such, must have a gateway that is specified in the IP address configuration. This information can be viewed on the LCD screen after the device is powered on (see the IP address configuration section). This port is used to make the web-based UI available outside the data subnet.

- Eth3 (`10GbE-B`) is used for the data transfer and can also be used for device management. This connection must either be on the same subnet as the source data, or can be directly connected to the server if needed.

Here is a cross reference of the ports presented in the UI and how they relate to the physical ports on the device.

![RJ45UI](/images/OSN5.2PortNamesRJ45.png)

### Configuring Copper SFP+ and RJ45

![Copper SFP+](/images/sfp-ports-sized-port5.png)

Ports originate from the device as Copper SFP+ and RJ45. Both CAT6A and Copper SFP+ cables are supplied.

- Eth5 (`10Gb SFP+ (5)`) is typically used for data transfer but can also be used for device management. This port runs only at 10-GbE speed.

- Eth2 (`10-GbE (2)`) is typically used for device management but can also be used for data transfer. This port can run at speeds of either 1 GbE or 10 GbE.


The data transfer connection must either be on the same subnet as the source data, or be directly connected to the server.

IP settings can be viewed and managed from the LCD screen after the device is powered on (see the IP address configuration section).

It is NOT required to configure and use both ports if the 10-GbE port's IP can be reached through a web browser.
{:note}

Here is a cross reference of the ports presented in the UI and how they relate to the physical ports on the device.

![SFPUI](/images/OSN5.2PortNamesSFP.png)

## Loading the Data

1.	The device arrives pre-configured with your IP address, user name, locked storage pool, and NFS share. The user password and storage pool password are communicated through a separate email.

2.	Determine the most appropriate place for the device to be placed. It needs to reach both power and your ethernet connections, and minimize foot traffic.

3.	Position the device to be connected. The device does not need to be removed from the portable case. It can remain in the transport case during use. Ensure that the device is at room temperature, and there's no condensation on it. Connect power by using the provided power cable underneath the case lid and power on the device.<br/>

    Take note of the two power switches.
    {:note}
    ![Power switches](/images/MDMSPowerSwitch.png)

4. Connect the device to the network.
    - Connecting RJ45
      1. Remove the CAT6A cable from the case lid and connect it to the Eth3 (10 GbE-B) port.
         ![Ports of the MDMS device](/images/MDMSNewEth1and3.png)
      2. Connect the provided CAT6A to SFP+ adapter and connect to your 10-Gb switch.
      3. If the IP address that is configured for Eth3 can be reached in the browser through `HTTPS://'Your-Eth3-IPAddress'`, continue to the next step. Otherwise, connect the Eth1 (`1GbE-B`) port.<br/>

         If you need to alter any IP settings for Eth3 or Eth1, see the [Configuring IP addresses](#configuring-ip-addresses) section.
         {:tip}

    - Connecting Copper SFP+
      1. Remove the Copper SFP+ cable from the case lid and connect it to Eth5 10 GbE (5)
         ![Ports of the MDMS device](/images/sfp-ports-sized-ports-labeled.png)
      2. Connect the Copper SFP+ cable to your 10-Gb switch.
      3. If the IP address that is configured for Eth5 can be reached through the browser `HTTPS://'Your-Eth5-IPAddress'`, continue to the next step, otherwise connect Eth2 (`10GbE-B` or `1GbE-B`) port.

         If you need to alter any IP settings for Eth5 or Eth2, see the [Configuring IP addresses](#configuring-ip-addresses) section.
         {:tip}

5. Open your browser, and enter `HTTPS://Your-Eth1-IPAddress`. Replace `Your-Eth1-IPAddress` with the Eth1 for your network configuration. Accept the certificate exception.

6. Use the provided user name and password to log in.<br/>
    ![Login page](/images/login.png)

7. The workflow wizard presents access to the specific items that are generally used in order from left to right.<br/>
    ![Workflow icons](/images/workflow.png)

    The workflow can be reopened by using the **Workflow Manager** in the upper-left area of the interface.
    {:tip}

8.	Activate the pre-configured storage pool.
    - Click **Unlock and Start Storage Pool**.
    - Enter your Storage Pool Passphrase, and click **OK**.
      ![Activate Storage Pool](/images/Unlock.png)

9. By default, the share has both NFS and SMB protocols that are enabled with no access restrictions. To restrict access to this share (for NFS or SMB), right-click the share name, and select the appropriate menu item.<br/>
   ![Restrict Share Access](/images/ShareAccessControl.png)

10. When the storage pool is enabled, the NFS share is available to mount. In the workflow, click **View Network Shares** to see the network shares view. Close the workflow, right-click the share, and select mount command to see the share name and mount information. Mount the share on your source server. Be sure to specify the 10-GB link IP address.
    ![Mounting the share](/images/MountCommand.png)

11. Copy your data to the NFS share. In the workflow, click **View Network Activity** to show inbound Ethernet load as data is transferred to the device on the 10-GB link.
    ![View activity](/images/SystemNetworkPerf.png)

12. In the workflow, click **View Storage pool** to monitor storage usage and IOPS on the device.
    ![View Storage Pool](/images/SystemStoragePoolPerf.png)

13.	When the load is complete, you can gracefully power down the system. In the workflow, click **Shutdown Appliance...**.
    ![Shutting Appliance Down](/images/SystemShutdown.png)

14.	Disconnect the device, return the power cable, Ethernet cable, and SFP+ adapter into their storage locations under the lid.

16.	Attach the provided shipping label, notify the carrier, and return device to the data center.


## Configuring IP addresses

The LCD screen on the device can be used to configure the IP addresses for the Ethernet ports. You move the cursor around in the LCD panel by using the **Up**, **Down**, **Back/ESC**, and **Forward/ENTER** buttons. **Enter** takes you into a menu and **Exit** takes you out.

When you edit an IP address or subnet mask, **Enter** steps you forward one character at a time; **Exit** steps you back one character at a time.

**Up** and **Down** toggles through the numbers for the elected location.

Use **Exit** to back up to the former menu.

Go to **Update...** and press **Enter** to save the setting.

  ![LCD Display](/images/MDMSLCD.png)
