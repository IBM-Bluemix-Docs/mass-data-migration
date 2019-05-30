---

copyright:
  years:  2019
lastupdated: "2019-05-16"

keywords:

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
{:download: .download}

# Managing your request
{: #manage-request}

Manage and track the status of your {{site.data.keyword.mdms_full}} order by using the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

## Tracking your order (beta)
{: #track-order}

After you request a device, you can track the progress of your order by using the {{site.data.keyword.mdms_short}} dashboard in the {{site.data.keyword.cloud_notm}} console. 

To access tracking information about your order, select **{{site.data.keyword.mdms_short}}** from your {{site.data.keyword.cloud_notm}} resource list, and then click the _Request details_ tab from the application details page.

This feature is available as part of the [{{site.data.keyword.mdms_short}} beta release](/docs/services/mass-data-migration?topic=mass-data-migration-beta). You can also track the status of your order by using the [{{site.data.keyword.mdms_short}} request details page](https://control.softlayer.com/storage/mdms){: external} that is available from the {{site.data.keyword.cloud_notm}} infrastructure portal.
{: note}

The following table shows how the order status changes as {{site.data.keyword.mdms_short}} processes the request.

| Status | Description |
| --- | --- |
| Processing order | After {{site.data.keyword.mdms_short}} receives the request, the status changes to _Processing order_. |
| Prepare shipment | After your order is approved, the request status changes to _Prepare shipment_. {{site.data.keyword.mdms_short}} prepares and configures the next available storage device.  |
| Ship to customer | A pre-configured storage device is shipped to your location. {{site.data.keyword.mdms_short}} uses roundtrip UPS overnight shipping for US devices and roundtrip FedEx overnight shipping for EU devices.|
| Client site | After the device is delivered to your location, the request status changes to _Client site_. |
| Coordinate shipment to IBM | **For regions outside of the US and EU.** If the device is delivered to a supported region outside of the US and EU, the request status changes to _Coordinate shipment with IBM_. Follow the instructions in the {{site.data.keyword.mdms_short}} dashboard to request a return shipment. |
| Ship to IBM | The device is in transit to IBM. |
| Data offload | When IBM receives the {{site.data.keyword.mdms_short}} device, the request status changes to _Data offload_. The device is connected to the network in the {{site.data.keyword.cloud_notm}} data center, and the data offload starts automatically.  |
| Erase data | When the offload process is complete, the request status changes to _Erase data_. Your data is now available in the Cloud Object Storage destination that you specified in the initial request. {{site.data.keyword.mdms_short}} permanently erases data from the device by using NIST data wipe standards. |
{: caption="Table 1. Describes the {{site.data.keyword.mdms_short}} order status workflow" caption-side="top"}
