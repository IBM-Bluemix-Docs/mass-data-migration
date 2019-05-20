---

copyright:
  years:  2019
lastupdated: "2019-05-14"

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

# Configuring the device
{: #configure-device}

{{site.data.keyword.mdms_full}} provides a portable, pre-configured storage device that is shipped to your location for easy migration of your data.
{: shortdesc}

Before you power on the {{site.data.keyword.mdms_short}} device, keep in mind the following considerations:

- Ensure that the device is at room temperature.
- Ensure that there is no condensation on the device.
- To avoid inadvertent damage to the device, keep the device in its portable case while the device is in use.

### Device overview
{: #device-overview}

Your {{site.data.keyword.mdms_short}} device arrives pre-configured and ready to connect to your network. 

The following image shows the main areas of the device.

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device-rj45.svg">
  <img src="images/mdms-device-rj45.svg" alt="Top-down view of the Mass Data Migration device">
</a>

{{site.data.keyword.cloud_notm}} provides two {{site.data.keyword.mdms_short}} device models. Each model comes packaged with [optics and adapters](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists) that support both RJ45 and SFP+ copper connections. 

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

Both device models offer the same functionality, but the cabling instructions are different for each model. When you receive your {{site.data.keyword.mdms_short}} device, be sure to identify the device model so that you follow the instructions that correspond to your device type.  

{{site.data.keyword.mdms_short}} devices use a [C13 power cord ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. If you're using the device outside of the United States, you might need an additional power adapter that accommodates the plug and socket system that is used in your country. {{site.data.keyword.mdms_short}} devices are compatible with all standard power ranges.
{: note}

## Powering on the device
{: #power-on-device}

After you position the device, use the supplied power cord to power on the device.

1. Retrieve the power cord that is located under the transport case lid.
2. Attach the power cord to the inlet on the device, and then connect the plug to a power socket.
3. Set the **Mains Switch** to **On**.
4. Power on the device by using the **System On / Off** button.

   When a System ID value displays on the _System Control Display_ screen, the device is powered on and ready for the next step.

## Reviewing your network settings
{: #review-network-settings}

You can review the network configuration on the device before you connect it to your network. View and manage the IP settings for your network ports by using the _System Control Display_ screen on the device. 

To interact with the _System Control Display_ screen, move the cursor by using the **△**, **▽**, **esc**, and **enter** buttons. **Enter** takes you into a menu and **esc** takes you out.
{: tip}

To edit an IP address or subnet mask:

1. From the Network Config menu, use the **△** and **▽** buttons to select the port that you want to modify. Press **enter**.
2. Select **IP Address**, and then use the **△** and **▽** buttons to set the new IP address.

   Press **enter** to move forward one character at a time. Press **esc** to move backwards one character at a time.
3. Press **esc** to return to the previous menu.
4. Go to **Update...** and press **enter** to save the setting.
