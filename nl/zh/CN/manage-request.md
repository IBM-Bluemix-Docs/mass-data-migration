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

# 管理请求
{: #manage-request}

使用 {{site.data.keyword.slportal}} 来管理和跟踪 {{site.data.keyword.mdms_full}} 订单的状态。
{: shortdesc}

通过参与 {{site.data.keyword.mdms_short}} Beta 程序，可以预览可通过 {{site.data.keyword.cloud_notm}} 控制台访问的新的 {{site.data.keyword.mdms_short}} 服务仪表板。要了解更多信息，请参阅[获取 Beta 访问权](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)。
{: tip}

## 跟踪订单 
{: #track-order}

请求存储设备后，可以使用 {{site.data.keyword.slportal}} 中提供的 [{{site.data.keyword.mdms_short}} 请求详细信息页面](https://control.softlayer.com/storage/mdms){: external}来跟踪订单的进度。

下表显示了订单状态在 {{site.data.keyword.mdms_short}} 处理请求的过程中如何变化。

|状态|描述|
| --- | --- |
|正在处理请求|{{site.data.keyword.mdms_short}} 收到请求后，状态会变为_正在处理请求_。|
|正在准备设备|核准订单后，请求状态会变为_正在准备设备_。{{site.data.keyword.mdms_short}} 会准备并配置下一个可用存储设备。|
|正在等待装运|预配置的存储设备正在等待装运到您所在的位置。请求进入_正在等待装运_状态后，即无法再取消订单。|
|设备已发货|承运方已取走存储设备并发往您所在的位置。您可以在[请求详细信息页面](https://control.softlayer.com/storage/mdms){: external}的_订单详细信息_部分中查看跟踪号。|
|设备已接收|设备返还到 {{site.data.keyword.cloud_notm}} 后，状态会变为_设备已接收_。|
|正在卸载数据|在数据传输过程中，请求状态会变为_正在卸载数据_。设备连接到 {{site.data.keyword.cloud_notm}} 数据中心内的网络，并且数据卸载会自动启动。|
|卸载完成|卸载过程完成后，请求状态会变为_卸载完成_。现在，数据在初始请求中指定的 Cloud Object Storage 目标中可用。|
|擦除完成|{{site.data.keyword.mdms_short}} 根据 NIST 数据擦除标准从设备中永久擦除数据。数据擦除过程完成后，订单状态会变为_擦除完成_。
{: caption="表 1. 描述 {{site.data.keyword.mdms_short}} 订单状态工作流程" caption-side="top"}
