---

copyright:
  years:  2019
lastupdated: "2019-05-09"

keywords:

subcollection: mass-data-migration

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Setting up the device
{: #set-up-device}

{{site.data.keyword.mdms_full}} provides a portable, pre-configured storage device that is shipped to your location for easy migration of your data.
{: shortdesc}

Before you power on and connect the {{site.data.keyword.mdms_short}} device, keep in mind the following considerations:

- Ensure that the device is at room temperature.
- Ensure that there is no condensation on the device.
- To avoid inadvertent damage to the device, keep the device in its portable case while the device is in use.

## Device overview
{: #device-overview}

{{site.data.keyword.cloud_notm}} ships the following {{site.data.keyword.mdms_short}} device models:

<table>
  <tr>
    <th>Device model</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><p><a href="#set-up-RJ45-model">RJ45</a></p></td>
    <td>
      <ul>
        <li>Natively supports Ethernet connectivity by using RJ45 connectors.</li>
        <li>Includes adapters and optics that enable SFP+ copper support.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><a href="#set-up-SFP+-model">RJ45 / SFP+</a></td>
    <td>
      <ul>
        <li>Natively supports both RJ45 and SFP+ copper connections.</li>
      </ul>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Table 1. Describes the supported {{site.data.keyword.mdms_short}} device models</caption>
</table>

Each model comes packaged with [optics and adapters](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists) that support both RJ45 and SFP+ copper connections. You can find the cables in pouches that are located inside the portable case.

The following image shows a top-down view of the RJ45 / SFP+ device model. 

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device.svg">
  <img src="images/mdms-device.svg" alt="Top-down view of the Mass Data Migration device">
</a>

{{site.data.keyword.mdms_short}} devices use a [C13 power cord ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. If you're using the device outside of the United States, you might need an additional power adapter that accommodates the plug and socket system that is used in your country. {{site.data.keyword.mdms_short}} devices are compatible with all standard power ranges.
{: note}

<!--![The figure shows a top view of the Mass Data Migration device.](images/mdms-device.svg){: caption="Figure 1. Shows a top-down view of the {{site.data.keyword.mdms_short}} device" caption-side="bottom"}-->

## Powering on the device
{: #power-on-device}

After you position the device, power on the device by using the supplied power cord.

1. Retrieve the power cord that is located under the transport case lid.
2. Attach the power cord to the inlet on the device, and then connect the plug to a power socket.
3. Set the **Mains Switch** to **On**.
4. Power on the device by using the **System On / Off** button.

   When a System ID value displays on the _System Control Display_ screen, the device is powered on and ready for the next step.

## Reviewing your network settings
{: #review-network-settings}

After you power on the device, you can view and manage the IP settings for your network ports from the _Network Config..._ menu on the device. 

![The figure shows the Network Config screen on the Mass Data Migration device.](images/network-config.svg){: caption="Figure 2. Shows the Network Config screen on the {{site.data.keyword.mdms_short}} device" caption-side="bottom"}

To interact with the _System Control Display_ screen, move the cursor by using the **△**, **▽**, **esc**, and **enter** buttons. **Enter** takes you into a menu and **esc** takes you out.
{: tip}

To edit an IP address or subnet mask:

1. From the Network Config menu, use the **△** and **▽** buttons to select the port that you want to modify. Press **enter**.
2. Select **IP Address**, and then use the **△** and **▽** buttons to set the new IP address.

   Press **enter** to move forward one character at a time. Press **esc** to move backwards one character at a time.

3. Press **esc** to return to the previous menu.

4. Go to **Update...** and press **enter** to save the setting.

## Connecting the device to your network
{: #connect-device}

To connect the device to your network, you need to configure two Ethernet connections. The first connection is for managing the device through a browser, and the second connection is for moving data across the same subnet where the source data is located.

Configuring Ethernet connectivity on the device depends on the {{site.data.keyword.mdms_short}} device type that you receive. 

To allow for greater efficiency in data transmission, [jumbo frames ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/Jumbo_frame){:new_window} are enabled by default on the 10 Gigabit Ethernet (10GbE) device ports. You can change this setting for your device by using the [Modify Network Port ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://wiki.osnexus.com/index.php?title=Network_Port_Modify) option in the user interface.
{: tip}

### Setting up the RJ45 model
{: #set-up-RJ45-model}

The RJ45 device model natively supports Ethernet connectivity by using RJ45 connectors. You can use the supplied CAT6A Ethernet cables to connect your storage system to the RJ45 network ports on the device. If you need to enable SFP+ copper support, use the supplied adapters. The adapters are compatible with all switch manufacturers. You can find the adapters in a pocket on the underside of the shipping container lid.

The following table shows how the physical ports on the device map to the ports that are displayed in the UI.

| Device port | Ethernet type  | UI display |  Description |
| --- | --- | --- | --- |
| Eth1 | 1GbE-B | `eno2` | The Eth1 port is used to manage the device and make the web-based UI available outside the data subnet. You can view the gateway information by using the _System Control Display_ screen after the device is powered on. |
| Eth3 | 10GbE-B | `eno4` | The Eth3 port is used to transfer data from your storage system onto the {{site.data.keyword.mdms_short}}. The connection must either be on the same subnet as the source data or directly connected to the server. |
{: caption="Table 2. Describes how {{site.data.keyword.mdms_short}} device ports map to the UI display" caption-side="top"}

To connect the device to your network by using the RJ45 connector:

1. Retrieve the CAT6A cable from the transport case lid.
2. Connect the CAT6A cable to the Eth3 (`10GbE-B`) port on the device.
3. Connect the CAT6A cable to the SFP+ adapter.
4. Connect the CAT6A cable to your 10Gb Ethernet switch.
5. Open a web browser, and navigate to the following URL.

   ```
   https://<your_Eth3_IP_address>
   ```
   {: codeblock}

   Replace `<your_Eth3_IP_address>` with the IP address that is configured for the Eth3 network port. To view the IP address, check the _System Control Display_ screen on the device.

6. Optional: If you can't reach the IP address, connect the CAT6A cable to the Eth1 (`1GbE-B`) port on the device and try again by navigating to the following URL.
   
   ```
   https://<your_Eth1_IP_address>
   ```
   {: codeblock}

   Replace `<your_Eth1_IP_address>` with the IP address that is configured for the Eth1 network port. To view the IP address, check the _System Control Display_ screen on the device.

   If you need to modify the IP settings for Eth3 or Eth1, see [Reviewing your network settings](#review-network-settings).
   {: tip}

### Setting up the RJ45 / SFP+ model
{: #set-up-SFP+-model}

The RJ45 / SFP+ device model natively supports both RJ45 and SFP+ copper connections, which means that the network ports originate from the device in both RJ45 and SFP+ copper formats. You can use the supplied CAT6A and SFP+ cables to connect your storage system to the network ports on the device. 

The following table shows how the physical ports on the device map to the ports that are displayed in the UI.

| Device port | Ethernet type  | UI display |  Description |
| --- | --- | --- | --- |
| Eth5 | 10Gb SFP+ | `eno3` | Th Eth5 port is used to transfer data from your storage system onto the {{site.data.keyword.mdms_short}}. This port can also be used to manage the device. The port runs only at 10GbE speed. |
| Eth2 | 10GbE | `eno6` | The Eth2 port is used to manage the device and make the web-based UI available outside the data subnet. This port can also be used for data transfer. The connection must either be on the same subnet as the source data or directly connected to the server. The port can run at speeds of either 1GbE or 10GbE. |
{: caption="Table 3. Describes how {{site.data.keyword.mdms_short}} device ports map to the UI display" caption-side="top"}

To connect the device to your network by using the SFP+ and RJ45 connectors:

1. Retrieve the SFP+ copper cable from the transport case lid.
2. Connect the SFP+ cable to the Eth5 (`10GbE (5)`) port on the device.
3. Connect the SFP+ cable to your 10Gb Ethernet switch.
4. Open a web browser, and navigate to the following URL.

   ```
   https://<your_Eth5_IP_address>
   ```
   {: codeblock}

   Replace `<your_Eth5_IP_address>` with the IP address that is configured for the Eth5 network port. To view the IP address, check the _System Control Display_ screen on the device.

5. Optional: If you can't reach the IP address, connect the SFP+ cable to the Eth2 (`10GbE-B` or `1GbE-B`) port on the device and try again by navigating to the following URL.
   
   ```
   https://<your_Eth2_IP_address>
   ```
   {: codeblock}

   Replace `<your_Eth2_IP_address>` with the IP address that is configured for the Eth2 network port. To view the IP address, check the _System Control Display_ screen on the device.

   If you need to alter any IP settings for Eth3 or Eth1, see the [Configuring IP addresses](#configuring-ip-addresses) section.
   {: tip}

## Accessing the user interface
{: #access-ui}

After you configure the device for Ethernet connectivity, you're ready to access the OSNEXUS QuantaStor user interface (UI) so you can begin loading and importing your data into the device.

To access the QuantaStor UI:

1. Open a web browser, and navigate to the following URL.

   ```
   https://<your_management_IP_address>
   ```
   {: codeblock}

   Replace `<your_management_IP_address>` with the IP address that is configured for your Eth1 or Eth2 network ports. Accept the certificate exception.

2. Log in to the QuantaStor UI by using the username and password that was sent to your e-mail address.

   ![Login page](/images/login.png)

   The Common Tasks wizard is displayed. Use the options from left to right to begin importing your data.

   ![Workflow icons](/images/workflow.png)

   You can reopen the Common Tasks wizard by using the **Workflow Manager** in the upper-left area of the interface.
   {:tip}

