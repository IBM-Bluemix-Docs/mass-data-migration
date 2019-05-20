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

# Service overview
{: #service-overview}

{{site.data.keyword.mdms_full}} provides a portable, pre-configured storage device that is shipped to your location for easy migration of your data.
{: shortdesc}

Learn about the different components that comprise the {{site.data.keyword.mdms_short}} service.

## Service components
{: #service-components}

{{site.data.keyword.mdms_short}} 

### {{site.data.keyword.mdms_short}} dashboard
{: #service-dashboard}

You can create and track {{site.data.keyword.mdms_short}} orders from the service dashboard in the {{site.data.keyword.cloud_notm}} console.


In the {{site.data.keyword.mdms_short}} dashboard, you specify your network configuration settings for the device, retrieve credentials to log in to the device, and track the status of your order.  

### {{site.data.keyword.mdms_short}} device
{: #storage-device}

{{site.data.keyword.mdms_short}} provides a portable storage device that is shipped to your location. The {{site.data.keyword.mdms_short}} device arrives pre-configured and ready to connect to your network. 

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

### File interface
{: #file-interface}

The file interface is a local, web-based UI that you use to access the network share on the {{site.data.keyword.mdms_short}} device. The file interface is based on a mature file and network software that enables large numbers of large files to be copied and transported to {{site.data.keyword.cloud_notm}}.

## Network configuration
{: #network-settings}

{{site.data.keyword.mdms_short}} devices are pre-configured for your network according to settings that you specify when you submit the device request. You can set your network configuration according to the following scenarios:

<dl>
    <dt>Default configuration</dt>
        <dd>The expected configuration for an MDMS device a 1Gb management port with a gateway and a 10Gb data port on the same subnet as the data source. This is represented on the order form.</dd>
    <dt>Optional configuration</dt>
        <dd>You can also allocate only the 10Gb port on the device for both data movement and device management connections. configure a 10Gb data transfer port with a gateway and no device management port. When you submit your , you can specify this configuration by providing the same IP, netmask, and gateway address for both the management and data ports. The device arrives with the 10Gb port configured with your IP information including a gateway.</dd>
<dl>

### Device management port
{: #device-management}

You can manage the {{site.data.keyword.mdms_short}} device by using a local, web-based file interface that you serve on your remote computer.


The device management port on the {{site.data.keyword.mdms_short}} device provides administrative access to the UI. To run the user interface, you connect your computer to the device management port on the device, and then reference the corresponding IP address in your browser. 

### Data transfer port
{: #device-management}

The data transfer port provides network share access that allows for data movement. When you mount the network share on the device to your source server, you reference the corresponding IP address for the data transfer port. The data transfer port can also serve as the device management port to run the file interface if needed.