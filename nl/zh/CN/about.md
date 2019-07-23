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

# 关于 {{site.data.keyword.mdms_short}}
{: #about}

通过 {{site.data.keyword.mdms_full}}，可快速、简单、安全地将太字节到拍字节数量级的数据物理传输到 {{site.data.keyword.cloud_notm}}。
{: shortdesc}

## 为什么选择 {{site.data.keyword.mdms_short}}？
{: #use-cases}

{{site.data.keyword.mdms_short}} 通过提供预先配置的便携式存储设备来轻松迁移数据，帮助您简化迁移到云的过程。请在以下视频中了解有关 {{site.data.keyword.mdms_short}} 功能和用例的更多信息。

<iframe class="embed-responsive-item" id="youtubeplayer" title="通过 Mass Data Migration，可快速、简单、安全地将数据传输到 IBM Cloud" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


|用例|描述|
| --- | --- |
|将数据迁移到云|无论您是想释放内部部署存储空间、归档不活动数据还是备份数据以实现冗余和恢复，{{site.data.keyword.mdms_short}} 都可以快速、安全地将您的数据移动到云中。|
|数据中心退役|在您缩小、扩展或搬迁数据中心时，快速启动数据中心变换，并使用 {{site.data.keyword.mdms_short}} 将敏感数据安全地移至云中。|
|有限带宽|进行数据传输时，如果您处于偏远地区，或者发现通过网络传输数据的选项成本高得离谱、速度太慢或不可用，那么 {{site.data.keyword.mdms_short}} 是一个非常不错的替代方法。|
{: caption="表 1. 描述 {{site.data.keyword.mdms_short}} 用例" caption-side="top"}

您可以通过[探索数据迁移解决方案](https://www.ibm.com/cloud/data-migration)来比较 {{site.data.keyword.cloud_notm}} 上的数据迁移选项。要了解有关 {{site.data.keyword.mdms_short}} 功能和优点的更多信息，请查看 [{{site.data.keyword.mdms_short}} 产品页面](https://www.ibm.com/cloud/mass-data-migration){: external}。
{: tip}

## 运作方式
{: #how-it-works}

{{site.data.keyword.mdms_short}} 使用可用容量为 120 TB 的存储设备来加速将数据移动到云，这克服了常见的传输难题，例如成本高、传输时间长和安全问题。

下图描述了 {{site.data.keyword.mdms_short}} 过程。

![描述 Mass Data Migration 过程。](images/mdms-workflow.png)

## 服务组件
{: #service-componenets}

{{site.data.keyword.mdms_short}} 包含以下服务组件。

<dl>
   <dt>{{site.data.keyword.mdms_short}} 仪表板</dt>
      <dd>可以在 <a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a> 的服务仪表板中创建和跟踪 {{site.data.keyword.mdms_short}} 订单。在 {{site.data.keyword.mdms_short}} 请求页面中，可指定设备的网络配置设置，检索凭证以登录到设备，以及跟踪订单的状态。</dd>
   <dt>{{site.data.keyword.mdms_short}} 设备</dt>
      <dd>{{site.data.keyword.mdms_short}} 提供了<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">便携式存储设备</a>，该设备可运送到您所在位置。{{site.data.keyword.mdms_short}} 设备到达时已预先配置，可随时连接到网络。</dd>
   <dt>设备用户界面</dt>
      <dd><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">设备用户界面</a>是一个基于 Web 的本地 UI，用于访问 {{site.data.keyword.mdms_short}} 设备上的网络共享。该 UI 基于成熟的文件和网络软件，支持将大量大型文件复制并传输到 {{site.data.keyword.cloud_notm}}。</dd>
</dl>










