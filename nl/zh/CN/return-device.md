---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# 返还设备
{: #return-device}

关闭 {{site.data.keyword.mdms_full}} 设备电源并将其返还到 {{site.data.keyword.cloud_notm}} 以完成迁移过程。
{: shortdesc}

## 断开设备连接
{: #disconnect-device}

数据复制过程完成后，可以正常关闭系统电源。

1. 在“常用任务”向导中，单击**关闭设备**。

    ![关闭设备](images/ShutDown.png)

    单击**确定**以确认。
2. 使用设备上的**开启/关闭系统**按钮来关闭设备电源。 
3. 将**主电源开关**设置为**关闭**。
4. 将所有电缆绕回线轴，然后与光学设备一起放回运输箱中相应的存储位置。

## 将设备运送到 {{site.data.keyword.cloud_notm}}
{: #ship-device}

在准备好返还设备时，准备装运标签并通知承运方。

1. 获取设备的清单列表和返还装运标签。这些文档位于运输箱箱盖内侧。

    如果要装运多个设备，请记住，每个运输箱中提供的返还装运标签是特定于存储设备的。在安排承运方提货之前，请确保将相应的返还装运标签粘贴到相应的设备。
    {: note}
2. 使用清单列表来验证是否所有电缆和光学设备都已放回运输箱中的相应存储位置。
3. 将清单列表放回运输箱，然后使用返还装运标签上列出的指示信息将标签粘贴到设备。
4. 安排承运方提货，并将设备返还到数据中心。

    设备返还到 {{site.data.keyword.cloud_notm}} 后，在 {{site.data.keyword.mdms_short}} 请求详细信息页面上，订单状态会变为_设备已接收_。

## 后续步骤
{: #return-device-next-steps}

- 通过[管理 {{site.data.keyword.mdms_short}} 请求](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)来检查订单的状态。
- 从源服务器中删除数据之前，请[验证数据是否已成功上传到 {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data)。

