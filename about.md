---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# About {{site.data.keyword.mdms_short}}
{: #about}

{{site.data.keyword.mdms_full}} is a fast, simple, and secure way to physically transfer terabytes to petabytes of data to {{site.data.keyword.cloud_notm}}.
{: shortdesc}

## Why {{site.data.keyword.mdms_short}}?
{: #use-cases}

{{site.data.keyword.mdms_short}} helps you simplify your journey to the cloud by providing a portable, pre-configured storage device for easy migration of data. Learn more about {{site.data.keyword.mdms_short}} features and use cases in following video.

<iframe class="embed-responsive-item" id="youtubeplayer" title="Mass Data Migration provides a fast, simple and secure way to transfer data to the IBM Cloud" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


| Use cases| Description |
| --- | --- |
| Migrating data to the cloud | Whether you want to free-up on-premises storage space, archive inactive data, or back up data for redundancy and recovery, {{site.data.keyword.mdms_short}} can quickly and securely move your data to the cloud. |
| Data center decommission | Jumpstart your data center transformation and use {{site.data.keyword.mdms_short}} to securely move your sensitive data to the cloud as you downsize, expand, or relocate your data center. |
| Limited bandwidth | {{site.data.keyword.mdms_short}} is a great alternative if you are in a remote location or find over-the-network options to be cost-prohibitive, too slow, or unavailable for your data transfer. |
{: caption="Table 1. Describes {{site.data.keyword.mdms_short}} use cases " caption-side="top"}

You can compare your data migration options on {{site.data.keyword.cloud_notm}} by [exploring our data migration solutions](https://www.ibm.com/cloud/data-migration). To learn more about {{site.data.keyword.mdms_short}} features and benefits, check out the [{{site.data.keyword.mdms_short}} product page](https://www.ibm.com/cloud/mass-data-migration){: external}.
{: tip}

## How it works
{: #how-it-works}

{{site.data.keyword.mdms_short}} uses 120 TB-usable capacity storage devices to accelerate moving data to the cloud and overcome common transfer challenges such as high costs, long transfer times, and security concerns.

The following image describes the {{site.data.keyword.mdms_short}} process.

![Describes the Mass Data Migration process.](images/mdms-workflow.png){: caption="Figure 1. Describes the Mass Data Migration workflow." caption-side="bottom"}

## Service components
{: #service-componenets}

{{site.data.keyword.mdms_short}} comprises the following service components.

<dl>
   <dt>{{site.data.keyword.mdms_short}} dashboard</dt>
      <dd>You can create and track {{site.data.keyword.mdms_short}} orders from the service dashboard in the <a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a>. In the {{site.data.keyword.mdms_short}} request page, you specify your network configuration settings for the device, retrieve credentials to log in to the device, and track the status of your order. </dd>
   <dt>{{site.data.keyword.mdms_short}} device</dt>
      <dd>{{site.data.keyword.mdms_short}} provides a <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">portable storage device</a> that is shipped to your location. The {{site.data.keyword.mdms_short}} device arrives pre-configured and ready to connect to your network.</dd>
   <dt>Device user interface</dt>
      <dd>The <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">device user interface</a> is a local, web-based UI that you use to access the network share on the {{site.data.keyword.mdms_short}} device. The UI is based on a mature file and network software that enables large numbers of large files to be copied and transported to {{site.data.keyword.cloud_notm}}.</dd>
</dl>







