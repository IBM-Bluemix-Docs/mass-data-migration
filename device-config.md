---

copyright:
  years:  2019
lastupdated: "2019-12-11"

keywords: copy data to device, move data to device 

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:preview: .preview}
{:term: .term}

# Device configuration
{: #device-config}

When you request a {{site.data.keyword.mdms_short}} device, you can choose from the following configuration options in the order form.
{: shortdesc}

| Option | Description |
|---|---|
| Pre-configure the device | **Recommended.** Provide network preferences, including IP addresses for the device, as part of the order form so that the device arrives ready to connect to your data center. |
| Manually configure the device | Configure network preferences for the device manually by [using the LCD screen](/docs/mass-data-migration?topic=mass-data-migration-verify-ip-settings#use-lcd-screen) after the device is delivered to your location. |

## Pre-configuring the device
{: #configure-before-shipping}

As a network admin, provide IP settings for the {{site.data.keyword.mdms_short}} device at the time of order placement based on your data center's security and performance requirements. 

{{site.data.keyword.mdms_short}} uses the IP information that you provide to configure the [device ports](#device-ports) for connectivity to your data center.
{: tip}

To configure the 10Gb data transfer port, you'll need:

- Static IP address
- Subnet mask for the server where your source data resides

To configure the 1GB device management port, you'll need:

- Static IP address
- Subnet mask
- Default gateway for the computer that will access the device GUI


## Configuring the device after delivery
{: #configure-after-delivery}

You can also set network preferences for the device after it arrives at your location. To change IP settings for the device, use the LCD screen. To find out more about changing IP addresses on the device, see [Verifying IP settings](/docs/mass-data-migration?topic=mass-data-migration-verify-ip-settings).