---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# {{site.data.keyword.cloud_notm}} Mass Data Migration 常见问题

## 问题 1. 什么是 {{site.data.keyword.cloud_notm}} Mass Data Migration？ 
{{site.data.keyword.cloud}} Mass Data Migration 是一种物理数据传输服务，使用可用容量为 120 TB 的坚固便携式存储设备，将太字节到拍字节的数据更快地安全移动到 {{site.data.keyword.cloud_notm}}。 

## 问题 2. 如何开始使用 Mass Data Migration？ 
使用 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}提交请求。一旦您的请求获得批准并经过处理后，将对接下来的一个或多个可用设备进行预配置，然后根据您的网络和送货信息发送给您。使用以下链接可立即开始：https://control.softlayer.com/storage/mdms

## 问题 3. 谁应该使用 Mass Data Migration？ 
Mass Data Migration 设备可配备为在几乎任何环境中运行，从数据中心和办公室一直到偏远地区、仓库和船舶。如果通过网络传输数据选项的成本太高、速度太慢或无法使用，那么 Mass Data Migration 也是一种替代方法。  

## 问题 4. 使用 Mass Data Migration 可以传输多少数据？
您可以传输的数据量几乎没有限制，不管是太字节还是拍字节的数据。每个设备最多可容纳 120 TB 可用容量（RAID-6 配置），但您可以使用多个设备来容纳更大的工作负载。

## 问题 5. 如何使用多个设备来移动超过 120 TB 的更大工作负载？ 
并行或串行使用多个设备可在单个迁移中移动所有数据，也可以使用单个设备进行迭代迁移。例如，并行使用 9 个设备来传输 1 PB 数据，或者使用单个设备进行 9 次单独的迁移。

## 问题 6. 传输数据需要多长时间？ 
从客户提交 Mass Data Migration 请求到其数据在 {{site.data.keyword.cos_full}} 存储区中可访问，这整个周转时间只要 7 天。

## 问题 7. 可以拥有 Mass Data Migration 设备多少时间？  
设备在现场的前 10 个工作日可免费保管。这不包括设备发货当日或收货当日。如果需要更长时间来完成数据获取，可以延长使用时间，但会按每天 30 美元收费（适用于美国和欧盟地区）。 

## 问题 8. Mass Data Migration 支持哪些网络接口？  
Mass Data Migration 设备具有带 RJ45 (CAT6a) 的 10 Gbps 网络接口 和 SFP+ 铜缆（含 RJ45 转 SFP+ 转换器）网络端口。

## 问题 9. Mass Data Migration 的缺省发货选项是什么？ 
Mass Data Migration 使用 UPS 次日达航空往返速递来运送所有设备。成本含在低廉的统一费率中：每个设备 395 美元。客户当前无法选择其他发货方式。

## 问题 10. 哪些区域提供 Mass Data Migration？ 
Mass Data Migration 仅在美国和欧盟提供。所有数据会分别迁移到服务的美国标准交叉区域层或欧盟交叉区域层中的 {{site.data.keyword.cos_full}}。设备不能从一个区域发货而返还到另一个区域。

## 问题 11. 将数据导入到 {{site.data.keyword.cloud_notm}} 的成本是多少？ 
将数据传输到 {{site.data.keyword.cloud_notm}} 中不会产生费用。

## 问题 12. 可以使用 Mass Data Migration 功能从 {{site.data.keyword.cloud_notm}} 导出数据吗？ 
Mass Data Migration 当前不支持从 {{site.data.keyword.cloud_notm}} 导出数据。

## 问题 13. Mass Data Migration 会对数据加密吗？ 
Mass Data Migration 使用 AES 256 位加密技术来加密所有数据，并提供高强度密码来解锁存储池。{{site.data.keyword.IBM}} 中的所有数据传输均通过 SSL 完成。

## 问题 14. Mass Data Migration 如何以物理方式确保数据安全？ 
所有 Mass Data Migration 设备都安装在坚固耐用的机箱中。这些机箱具有防水、防震和防篡改功能，可确保往返途中设备和数据的安全。 

## 问题 15. 如何在整个迁移过程中跟踪我的请求？ 
要跟踪请求的状态，请参阅 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}中 Mass Data Migration 页面上的“活动请求”部分。您可以使用以下链接登录到该门户网站：https://control.softlayer.com/storage/mdms

## 问题 16. 在将数据卸载到 {{site.data.keyword.cos_full_notm}} 之后，如何从设备中擦除这些数据？
数据卸载到 {{site.data.keyword.cos_full}} 完成后，{{site.data.keyword.IBM}} 会立即启动四遍 DOD 级别的数据擦除，以永久擦除设备中的数据。 

## 问题 17. Mass Data Migration 上的文件接口是什么？ 
Mass Data Migration 使用网络文件系统 (NFS)。

## 问题 18. 如何在 Mass Data Migration 上使用文件接口？ 
解锁加密池后，在包含要迁移的数据的服务器上安装 NFS 共享，然后开始将数据文件复制到 NFS 共享中。

## 问题 19. Mass Data Migration 上的文件接口有哪些优点？ 
该文件接口基于成熟的文件和网络软件，可以将大量大型文件复制并传输到 {{site.data.keyword.cloud_notm}}。

## 问题 20：如何在 Mass Data Migration 设备上存储文件？ 
Mass Data Migration 设备使用采用 LZ4 压缩和 AES 256 位加密的 ZFS 文件系统。

## 问题 21. 在美国使用 Mass Data Migration 需要多少成本？ 
在美国，按每台设备 395 美元的统一费率收费，其中包含 295 美元设备费、100 美元往返 UPS 次日达空运速递费和 10 个工作日在您现场的使用费。 

## 问题 22. 使用 {{site.data.keyword.cos_full_notm}} 要收费吗？ 
将数据传输到 {{site.data.keyword.cloud_notm}} 是免费的，但标准费率适用于存储在 {{site.data.keyword.cos_full}} 中或其他任何 {{site.data.keyword.cloud_notm}} 服务中的数据。您可以通过以下链接找到 {{site.data.keyword.cos_full}} 标准交叉区域产品的定价：https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## 问题 23. 可以购买 {{site.data.keyword.cloud_notm}} Mass Data Migration 设备吗？ 
{{site.data.keyword.cloud_notm}} Mass Data Migration 设备不可购买。 
