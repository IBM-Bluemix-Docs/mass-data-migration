---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

Manage and track the status of your {{site.data.keyword.mdms_full}} order by using the {{site.data.keyword.slportal}}.
{: shortdesc}

By participating in the {{site.data.keyword.mdms_short}} beta program, you can preview a new {{site.data.keyword.mdms_short}} service dashboard that you can access from the {{site.data.keyword.cloud_notm}} console. To find out more, see [Getting access to beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Tracking your order 
{: #track-order}

After you request a storage device, you can track the progress of your order by using the [{{site.data.keyword.mdms_short}} request details page](https://control.softlayer.com/storage/mdms){: external} that is available from the {{site.data.keyword.slportal}}.

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
