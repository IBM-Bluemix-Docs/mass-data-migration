---

copyright:
  years: 2017, 2020
lastupdated: "2020-06-18"

keywords: activity tracker, LogDNA, monitor MDMS events

subcollection: mass-data-migration


---
{:new_window: target="_blank"}
{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:download: .download}
{:table: .aria-labeledby="caption"}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}

# Auditing events for Mass Data Migration
{: #at-events}

Use the {{site.data.keyword.at_full}} service to track activity that occurs with {{site.data.keyword.mdms_short}}.
{: shortdesc}

The {{site.data.keyword.at_full_notm}} service records when people place {{site.data.keyword.mdms_short}} orders, as well as each order's status changes.
For more information, see [{{site.data.keyword.at_full_notm}}](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-getting-started).  

You can use this service to investigate abnormal activity and critical actions, and to comply with regulatory audit requirements. In addition, you can be alerted about actions as they happen. The events that are collected comply with the Cloud Auditing Data Federation (CADF) standard.

## Global events
{: #at-actions-global}

{{site.data.keyword.mdms_short}} generates a single, global event that occurs on the state transitions of {{site.data.keyword.mdms_short}} orders. This event is global. You can monitor these events through the Activity Tracker instance that is available in the Frankfurt location.

The event `mass-data-migration.status.update` is generated on order changes. To see the state the order was transitioned to, look under `requestData`. `updateType` will be set to "status changed". The status the order is changing from will be in `initialValue`, the status it is changed to is in `finalValue`.

The table below shows the order status values you can see, and a description of each. 

| Action               | Description                               |
|----------------------|-------------------------------------------|
| processing           | The order is awaiting approval  |
| canceled             | The order has been canceled   |
| prepareShipment      | The order has been approved, preparing device for shipment   |
| shipToCustomer       | IBM has shipped the device to the customer |
| clientSite           | The device is at the client site |
| coordinateShipToIBM  | The device is being coordinated to be shipped back to IBM |
| shipToIBM            | The customer has shipped the device back to IBM |
| offload              | The device data is being uploaded into COS |
| eraseData            | The device is being securely erased |
| completed            | The order has completed |
| rejected             | The order has been rejected |

{: caption="Table 1. {{site.data.keyword.mdms_short}} actions that generate global events"}


## Viewing events
{: #at-ui}

You can view the Activity Tracker events that are associated with your {{site.data.keyword.mdms_short}} instance by using [{{site.data.keyword.at_full_notm}}](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-getting-started).

You can only provision 1 instance of the {{site.data.keyword.at_full_notm}} service per location.

To view events, you must identify the location where events are collected and available for monitoring. Then, you must access the web UI of the {{site.data.keyword.at_full_notm}} instance in that location. For more information, see [Launching the web UI through the IBM Cloud UI](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-launch#launch_step2).

{{site.data.keyword.mdms_short}} global events are forwarded to the {{site.data.keyword.at_full_notm}} service instance that is located in Frankfurt.
