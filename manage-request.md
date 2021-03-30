---

copyright:
  years: 2017, 2021
lastupdated: "2021-03-30"

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
{:preview: .preview}
{:term: .term}

# Managing your request
{: #manage-request}

Manage and track the status of your {{site.data.keyword.mdms_full}} order by using the {{site.data.keyword.slportal}}.
{: shortdesc}


## Tracking your order 
{: #track-order}

After you request a storage device, you can track the progress of your order by using the {{site.data.keyword.mdms_short}} dashboard that is available from the IBM Cloud console.

If you order multiple {{site.data.keyword.mdms_short}} devices, each order appears in the **Services** section of your IBM Cloud resource list.
{: tip}

## Managing your import request 
{: #manage-import-request}

The following table shows how the order status changes as {{site.data.keyword.mdms_short}} processes a request to import your data from your on-prem storage to the cloud.

| Status | Description |
| --- | --- |
| Processing order | After {{site.data.keyword.mdms_short}} receives the request, the status changes to _Processing order_. |
| Prepare shipment | After your order is approved, the request status changes to _Prepare shipment_. {{site.data.keyword.mdms_short}} prepares and configures the next available storage device.  |
| Ship to customer | A pre-configured storage device is shipped to your location. {{site.data.keyword.mdms_short}} uses roundtrip UPS overnight shipping for US devices and roundtrip FedEx overnight shipping for EU devices.|
| Client site | After the device is delivered to your location, the request status changes to _Client site_. |
| Coordinate shipment to IBM | **For regions outside of the US, EU, United Kingdom, and Canada.** If the device is delivered to a supported region outside of the US, EU, United Kingdom, or Canada, the request status changes to _Coordinate shipment with IBM_. [Create a support case](/docs/mass-data-migration?topic=mass-data-migration-return-device#return-device-from-other-regions) to request a pickup and return shipment. |
| Ship to IBM | The device is in transit to IBM. |
| Data offload | When IBM receives the {{site.data.keyword.mdms_short}} device, the request status changes to _Data offload_. The device is connected to the network in the {{site.data.keyword.cloud_notm}} data center, and the data offload starts automatically.  |
| Erase data | When the offload process is complete, the request status changes to _Erase data_. Your data is now available in the Cloud Object Storage destination that you specified in the initial request. {{site.data.keyword.mdms_short}} permanently [erases](/docs/mass-data-migration?topic=mass-data-migration-data-security#security-deletion) data from the device. |
| Complete | Your order was successfully completed. |
{: caption="Table 1. Describes the {{site.data.keyword.mdms_short}} order status workflow" caption-side="top"}

## Managing your export request 
{: #manage-export-request}

The following table shows how the order status changes as {{site.data.keyword.mdms_short}} processes a request to export your data from the cloud to your on-prem storage.

| Status | Description |
| --- | --- |
| Processing order | After {{site.data.keyword.mdms_short}} receives the request, the status changes to _Processing order_. |
| Data offload | After your order is approved, a device is connected to the network and data from your COS Bucket is copied to the device. |
| Prepare shipment | {{site.data.keyword.mdms_short}} prepares and configures storage device. |
| Ship to customer | A pre-configured storage device is shipped to your location. {{site.data.keyword.mdms_short}} uses roundtrip UPS overnight shipping for US devices and roundtrip FedEx overnight shipping for EU devices.|
| Client site | After the device is delivered to your location, the request status changes to _Client site_. |
| Coordinate shipment to IBM | **For regions outside of the US, EU, United Kingdom, and Canada.** If the device is in a supported region outside of the US, EU, United Kingdom, or Canada, the request status changes to _Coordinate shipment with IBM_. [Create a support case](/docs/mass-data-migration?topic=mass-data-migration-return-device#return-device-from-other-regions) to request a pickup and return shipment. |
| Data Export in EU Region | When you are exporting data across country borders within the EU region, you are required to provide the Export Control Classification Number (ECCN) or a Wassenaar Equivalent number. You are also required to specify if you require a license to export data across the border. If you do not know this information, please connect with an export regulation professional within your organization to help you figure out your Export Classification information. |
| Ship to IBM | The device is in transit to IBM. |
| Erase Data | All traces of your data are permanently [erased](/docs/mass-data-migration?topic=mass-data-migration-data-security#security-deletion) from the device. |
| Complete | Your order was successfully completed. |
{: caption="Table 2. Describes the {{site.data.keyword.mdms_short}} export order status workflow" caption-side="top"}
<!--- Cannot see a difference between the format of Table 1 & Table 2 captions.-->