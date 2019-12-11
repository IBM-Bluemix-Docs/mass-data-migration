---

copyright:
  years:  2019
lastupdated: "2019-12-11"

keywords: device models, device ports, network settings, configure network  

subcollection: mass-data-migration

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:external: target="_blank" .external}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:preview: .preview}
{:term: .term}

# Device overview
{: #device-overview}

Learn about {{site.data.keyword.mdms_full}} device models and network configuration options. 
{: shortdesc}

The following image shows the main areas of the device.

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device-rj45.svg">
  <img src="images/mdms-device-rj45.svg" alt="Top-down view of the Mass Data Migration device">
</a>

## Device models
{: #device-models}

{{site.data.keyword.cloud_notm}} provides two {{site.data.keyword.mdms_short}} device models. Each model comes packaged with [optics and adapters](/docs/mass-data-migration?topic=mass-data-migration-inventory-checklists) that support both RJ45 and SFP+ copper connections. 


<table>
  <tr>
    <th>Device model</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><p><a href="/docs/mass-data-migration?topic=mass-data-migration-connect-device#set-up-RJ45-model">RJ45</a></p></td>
    <td>
      <ul>
        <li>Natively supports Ethernet connectivity by using RJ45 connectors.</li>
        <li>Includes adapters and optics that enable SFP+ copper support.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><p><a href="/docs/mass-data-migration?topic=mass-data-migration-connect-device#set-up-SFP+-model">RJ45 / SFP+</a></p></td>
    <td>
      <ul>
        <li>Natively supports both RJ45 and SFP+ copper connections.</li>
      </ul>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Table 1. Describes the supported {{site.data.keyword.mdms_short}} device models</caption>
</table>

Both device models offer the same functionality, but the cabling instructions are different for each model. When you receive your {{site.data.keyword.mdms_short}} device, be sure to identify the device model so that you follow the instructions that correspond to your device type.  

{{site.data.keyword.mdms_short}} devices use a [C13 power cord](https://en.wikipedia.org/wiki/IEC_60320){: external}. If you're using the device outside of the United States, you might need an additional power adapter that accommodates the plug and socket system that is used in your country. {{site.data.keyword.mdms_short}} devices are compatible with all standard power ranges.
{: note}

## Device ports
{: #device-ports}

{{site.data.keyword.mdms_short}} devices are configured for two Ethernet connections. The first connection handles device management by running a web-based user interface, and the second connection handles data movement between the device and your source server.

By having two connections between the device and your server, you separate network management on the device from its data path. To achieve this separation, ensure that the management connection is on a different [subnet](#x2040149){: term} than the data connection.
{: tip}

<dl>
    <dt>1Gb Device management port</dt>
        <dd>You can manage the {{site.data.keyword.mdms_short}} device by using a local, web-based device interface that you serve on your remote computer. The device management port on the {{site.data.keyword.mdms_short}} device provides administrative access to the UI. To run the user interface, you connect your computer to the device management port on the device, and then reference the corresponding IP address in your browser.</dd>
    <dt>10Gb Data transfer port</dt>
        <dd>The data transfer port handles data movement from your storage system onto the {{site.data.keyword.mdms_short}} device. The port runs at 10Gb speed.</dd>
</dl>

## Network configuration
{: #network-settings}

You can prepare the device for connectivity to your network in one of two ways:

<dl>
  <dt>Using the 1Gb and 10Gb ports (Recommended)</dt>
    <dd>You can connect the device using the <a href="#device-ports">1Gb and 10Gb device ports</a> on different subnets, where only the device management port gets a gateway. For example, use the 1Gb port (on subnet <code>xx.xx.xx.xx</code>) with a gateway, and the 10Gb port on the same subnet as the data source (on subnet <code>yy.yy.yy.yy</code>).</dd>
  <dt>Using only the 10Gb port</dt>
    <dd>You can also use only the 10Gb port on the device for both data movement and device management connections. When you request a {{site.data.keyword.mdms_short}} device, you can specify this configuration in the order form by leaving the 1Gb fields blank. The device arrives with the 10Gb port that is configured with your IP information, including a gateway.</dd>
    <dd><p class="note">Configuring a gateway on both the device management port and the data transfer port is not supported. If you need to configure routing on the data transfer port by adding a gateway (not recommended), you must also be able to reach the IP address for the data transfer port from your browser to run the device user interface.</p></dd>
