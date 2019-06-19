---

copyright:
  years:  2019
lastupdated: "2019-06-19"

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

Manage and track the status of your {{site.data.keyword.mdms_full}} order by using the {{site.data.keyword.cloud_notm}} infrastructure portal.
{: shortdesc}

By participating in the {{site.data.keyword.mdms_short}} beta program, you can preview a new {{site.data.keyword.mdms_short}} service dashboard that you can access from the {{site.data.keyword.cloud_notm}} console. To find out more, see [Getting access to beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Tracking your order 
{: #track-order}

After you request a storage device, you can track the progress of your order by using the [{{site.data.keyword.mdms_short}} request details page](https://control.softlayer.com/storage/mdms){: external} that is available from the {{site.data.keyword.cloud_notm}} infrastructure portal.

The following table shows how the order status changes as {{site.data.keyword.mdms_short}} processes the request.

| Status | Description |
| --- | --- |
| Processing Request | After {{site.data.keyword.mdms_short}} receives the request, the status changes to _Processing request_. |
| Prepping Device | After your order is approved, the request status changes to _Prepping device_. {{site.data.keyword.mdms_short}} prepares and configures the next available storage device.  |
| Awaiting Shipment | The pre-configured storage device is awaiting shipment to your location. After the request enters _Awaiting shipment_ status, the order can no longer be cancelled. |
| Device Shipped | The storage device is picked up by the carrier and shipped to your location. You can view the tracking number in the _Order Details_ section of the [request details page](https://control.softlayer.com/storage/mdms){: external}. |
| Device Received | After the device is returned to {{site.data.keyword.cloud_notm}}, the status changes to _Device Received_. |
| Offloading Data | During the data transfer process, the request status changes to _Offloading Data_. The device is connected to the network in the {{site.data.keyword.cloud_notm}} data center, and the data offload starts automatically.  |
| Offload Complete| When the offload process is complete, the request status changes to _Offload complete_. Your data is now available in the Cloud Object Storage destination that you specified in the initial request. |
| Erase Complete | {{site.data.keyword.mdms_short}} permanently erases data from the device by using NIST data wipe standards. After the data erasure process is complete, the order status changes to _Erase Complete_.
{: caption="Table 1. Describes the {{site.data.keyword.mdms_short}} order status workflow" caption-side="top"}

<!-- Post beta
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
-->
