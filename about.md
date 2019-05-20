---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-16"

keywords:

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}


# About {{site.data.keyword.mdms_short}}
{: #about}

{{site.data.keyword.mdms_full}} is a fast, simple, and secure way to physically transfer terabytes to petabytes of data to {{site.data.keyword.cloud_notm}}.
{: shortdesc}

## {{site.data.keyword.mdms_short}} use cases
{: #use-cases}

When you need to securely transfer a large amount of data into the cloud, you can use {{site.data.keyword.mdms_short}} to jumpstart the migration process. Find out more about {{site.data.keyword.mdms_short}} features and use cases in following video.

<iframe class="embed-responsive-item" id="youtubeplayer" title="Mass Data Migration provides a fast, simple and secure way to transfer data to the IBM Cloud" type="text/html" width="640" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


| Use case | Description |
| --- | --- |
| Migrating data to the cloud | Whether you want to free-up on-premises storage space, archive inactive data, or backup data for redundancy and recovery, {{site.data.keyword.mdms_short}} can quickly and securely move your data to the cloud. |
| Data center decommission | Jumpstart your data center transformation and use {{site.data.keyword.mdms_short}} to securely move your sensitive data to the cloud as you downsize, expand, or relocate your data center. |
| Limited bandwidth | {{site.data.keyword.mdms_short}} is a great alternative if you are in a remote location or find over-the-network options to be cost-prohibitive, too slow, or unavailable for your data transfer. |
{: caption="Table 1. Describes {{site.data.keyword.mdms_short}} use cases " caption-side="top"}

## How it works
{: #how-it-works}

{{site.data.keyword.mdms_short}} uses 120 TB-usable capacity storage devices to accelerate moving data to the cloud and overcome common transfer challenges such as high costs, long transfer times, and security concerns.

The following flowchart walks you through the {{site.data.keyword.mdms_short}} process.

`TBU`


## Service components
{: #service-components}

Learn about the different components that comprise the {{site.data.keyword.mdms_short}} service.

### {{site.data.keyword.mdms_short}} dashboard
{: #service-dashboard}

You can create and track {{site.data.keyword.mdms_short}} orders from the service dashboard in the {{site.data.keyword.cloud_notm}} console.

In the {{site.data.keyword.mdms_short}} dashboard, you specify your network configuration settings for the device, retrieve credentials to log in to the device, and track the status of your order.  

### {{site.data.keyword.mdms_short}} device
{: #storage-device}

{{site.data.keyword.mdms_short}} provides a portable storage device that is shipped to your location. The {{site.data.keyword.mdms_short}} device arrives pre-configured and ready to connect to your network. 

{{site.data.keyword.cloud_notm}} provides two {{site.data.keyword.mdms_short}} device models. Each model comes packaged with [optics and adapters](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists) that support both RJ45 and SFP+ copper connections.
{: note} 

### File interface
{: #file-interface}

The file interface is a local, web-based UI that you use to access the network share on the {{site.data.keyword.mdms_short}} device. The file interface is based on a mature file and network software that enables large numbers of large files to be copied and transported to {{site.data.keyword.cloud_notm}}.

## Benefits and features
{: #mdms-benefits}

{{site.data.keyword.mdms_short}} offers the following benefits and features.

<dl>
   <dt>Fast data migration</dt>
      <dd>By using a single {{site.data.keyword.mdms_short}} device, you can migrate up to 120 TB of data (at RAID-6) in just days, as opposed to weeks or months that traditional data transfer methods use.</dd>
   <dt>Flexible and scalable</dt>
      <dd>Whether you need to migrate a few terabytes or many petabytes of data, you have the flexibility to request one or multiple devices to accommodate your workload.</dd>
   <dt>Affordable rates</dt>
      <dd>Moving large data sets can be expensive and time-consuming. Each {{site.data.keyword.mdms_short}} device is offered at an affordable rate that includes roundtrip shipping and 10 days of use at your site.</dd>
   <dt>Simple process</dt>
      <dd>{{site.data.keyword.IBM}} sends you a pre-configured device for you to connect, ingest data, and then send back to {{site.data.keyword.IBM}} for offload into {{site.data.keyword.cos_full}}. When the offload is complete, you can enjoy immediate access to your data in the cloud while {{site.data.keyword.BluSoftlayer}} securely wipes the device.</dd>
   <dt>End-to-end protection</dt>
      <dd>Device design maximizes security from the inside-out by using AES 256-bit encryption, RAID-6 configuration and rugged, tamper-evident, waterproof, shockproof cases to promote data protection and integrity during device-handling and transport.</dd>
   <dt>Secure erasure</dt>
      <dd>{{site.data.keyword.IBM}} uses a four-pass, DOD-Level data wipe to ensure complete erasure of all customer data from {{site.data.keyword.mdms_short}} devices.</dd>
</dl>





