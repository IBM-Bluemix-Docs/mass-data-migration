---

copyright:
  years: 2017, 2018
lastupdated: "2018-09-19"

---
{:new_window: target="_blank"}

# 常见问题

## **什么是 {{site.data.keyword.cloud_notm}} Mass Data Migration？**

{{site.data.keyword.cloud}} Mass Data Migration 是一种物理数据传输服务，使用可用容量为 120 TB 的坚固便携式存储设备，将太字节到拍字节的数据更快地安全移动到 {{site.data.keyword.cloud_notm}}。

<hr/>

## **如何启动 Mass Data Migration？**

使用 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 提交请求。您的请求获得批准并经过处理后，将对接下来的一个或多个可用设备进行配置，然后根据您的网络和发货信息发送给您。使用以下链接可立即开始：https://control.softlayer.com/storage/mdms

<hr/>

## **为什么要使用 Mass Data Migration？**

Mass Data Migration 设备可配备为在几乎任何环境中运行，从数据中心和办公室一直到偏远地区、仓库和船舶。此外，如果通过网络传输数据的选项的成本太高、速度太慢或不可用，那么也可将 Mass Data Migration 作为一种替代方法。

<hr/>

## **使用 Mass Data Migration 可以传输多少数据？**

您可以传输的数据量几乎没有限制，不管是太字节还是拍字节的数据。每个设备最多可容纳 120 TB 可用容量（RAID-6 配置），但您可以使用多个设备来容纳更大的工作负载。最大的单个对象限制为 10 TB。

<hr/>

## **可以使用多个设备来移动超过 120 TB 的更大型工作负载吗？如果可以，该如何做？**

并行或串行使用多个设备可在单个迁移中移动所有数据，也可以使用单个设备进行迭代迁移。例如，并行使用 9 个设备来传输 1 PB 数据，或者使用单个设备进行 9 次单独的迁移。

<hr/>

## **传输数据需要多长时间？**

从客户提交 Mass Data Migration 请求到其数据在 {{site.data.keyword.cos_full}} 存储区中可访问，这整个周转时间只要 7 天。传输性能受要传输的文件数的影响。传输数百万个小文件所用的时间要长于传输包含相同数据量但数量相对较少的文件。

<hr/>

## **Mass Data Migration 设备可以保留多长时间？**

设备可在现场免费保留前 10 个工作日。此时间范围不包括设备发货当日或收货当日。如果需要更长时间来完成数据获取，可以延长使用时间，但会按每天 30 美元收费（适用于美国和欧盟地区）。

<hr/>

## **Mass Data Migration 支持哪些网络接口？**

Mass Data Migration 设备具有带 RJ45 (CAT6a) 的 10 Gbps 网络接口和 SFP+ 铜缆网络端口。包含 RJ45 到 SFP+ 转换器。对于 10 Gbps 接口，已启用巨型帧。

<hr/>

## **Mass Data Migration 的缺省发货选项是什么？**

Mass Data Migration 使用 UPS 次日达航空往返速递来运送所有设备。成本含在每个设备 395 美元的低廉统一费率中。客户当前无法选择其他发货方式。

<hr/>

## **哪些区域提供 Mass Data Migration？**

Mass Data Migration 仅在美国和欧盟提供。所有数据会迁移到服务的美国标准交叉区域层或欧盟交叉区域层中的 {{site.data.keyword.cos_full}}。设备不能从一个区域发货而返还到另一个区域。

<hr/>

## **将数据导入到 {{site.data.keyword.cloud_notm}} 的成本是多少？**

将数据传输到 {{site.data.keyword.cloud_notm}} 中不会产生费用。

<hr/>

## **Mass Data Migration 可以用于从 {{site.data.keyword.cloud_notm}} 导出数据吗？**

Mass Data Migration 当前不支持从 {{site.data.keyword.cloud_notm}} 导出数据。

<hr/>

## **Mass Data Migration 会对数据加密吗？**

Mass Data Migration 使用 AES 256 位加密技术来加密所有数据，并提供高强度密码来解锁存储池。{{site.data.keyword.IBM}} 中的所有数据传输均通过 SSL 完成。

<hr/>

## **Mass Data Migration 如何以物理方式确保数据安全？**

所有 Mass Data Migration 设备都安装在坚固耐用的机箱中。这些机箱具有防水、防震和防篡改功能，可确保往返途中设备和数据的安全。

<hr/>

## **如何在整个迁移过程中跟踪请求？**

要跟踪请求的状态，请参阅 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中 Mass Data Migration 页面上的“活动请求”部分。您可以使用以下链接登录到该门户网站：https://control.softlayer.com/storage/mdms

<hr/>

## **将数据卸载到 {{site.data.keyword.cos_full_notm}} 后如何擦除数据？**

数据卸载到 {{site.data.keyword.cos_full}} 完成后，{{site.data.keyword.IBM}} 会立即启动四遍 DOD 级别的数据擦除，以永久擦除设备中的数据。

<hr/>

## **文件接口是什么？**

缺省情况下，Mass Data Migration 设备具有启用了网络文件系统 (NFS) 和服务器消息块 (SMB) 的共享。

<hr/>

## **如何使用文件接口？**

首先，解锁加密池。然后，在包含要迁移的数据的服务器上安装共享。开始将数据文件复制到共享。

<hr/>

## **Mass Data Migration 上的文件接口有哪些优点？**

该文件接口基于成熟的文件和网络软件，可以将大量大型文件复制并传输到 {{site.data.keyword.cloud_notm}}。

<hr/>

## **如何在 Mass Data Migration 设备上存储文件？**

Mass Data Migration 设备使用采用 LZ4 压缩和 AES 256 位加密的 ZFS 文件系统。

<hr/>

## **在美国使用 Mass Data Migration 需要多少成本？**

在美国，按每台设备 395 美元的统一费率收费。此成本包含 295 美元设备费、100 美元往返 UPS 次日达空运速递费和 10 个工作日在贵方现场的使用费。

<hr/>

## **{{site.data.keyword.cos_full_notm}} 使用成本是多少？**

将数据传输到 {{site.data.keyword.cloud_notm}} 是免费的。但是，标准费率适用于存储在 {{site.data.keyword.cos_full}} 中或其他任何 {{site.data.keyword.cloud_notm}} 服务中的数据。您可以通过以下链接找到 {{site.data.keyword.cos_full}} 标准交叉区域产品的定价：https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

<hr/>

## **可以购买 {{site.data.keyword.cloud_notm}} Mass Data Migration 设备吗？**

{{site.data.keyword.cloud_notm}} Mass Data Migration 设备恕不出售。
