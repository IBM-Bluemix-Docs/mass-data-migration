---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: copy data to device, move data to device, 

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

# 将数据复制到设备
{: #copy-data}

您可以使用设备用户界面将数据复制到 {{site.data.keyword.mdms_full}} 设备。

## 将数据复制到设备
{: #copy-data}

将服务器连接到网络共享后，可以启动并监视将数据复制到设备的过程。

1. 使用与主机兼容的文件复制工具将数据复制到网络共享上。
2. 在“常用任务”向导中，单击**查看网络活动**可显示数据通过 10 Gb 链路传输到设备时的入站以太网负载。
   
    ![查看活动](images/NetworkPerf.png)
3. 单击**查看存储池**可监视设备上的存储器使用情况和 IOPS。
   
    ![查看存储池](images/PoolPerf.png)

## 后续步骤
{: #import-data-next-steps}

- 正常[关闭设备电源](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device)。
- 准备装运标签并[将设备返还到 {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device)。
