---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# {{site.data.keyword.cloud_notm}} Mass Data Migration 概述

通过物理方式将太字节到拍字节的数据传输到 {{site.data.keyword.Bluemix}}，既快速简单又安全。

## 什么是 Mass Data Migration？

Mass Data Migration 使用可用容量为 120 TB 的存储设备来加速将数据移动到云，这克服了常见的传输难题，例如高成本、传输时间长和安全问题 - 所有这些难题通过一项服务得到解决。

![Mass Data Migration 过程流](/images/MDMSWorkflow.png)

## Mass Data Migration 优点
1. 快速移动数据
    - 使用单个 Mass Data Migration 设备，可以在几天内就迁移高达 120 TB 的数据（RAID-6 配置），而使用传统数据传输方法需要数周或数月时间。
2. 灵活且可扩展
    - 无论您需要迁移的是几个太字节还是几个拍字节的数据，都可以灵活地请求一个或多个设备来容纳您的工作负载。
3. 经济实惠
    - 移动大型数据集可能成本高、耗时长。每个 Mass Data Migration 设备均以经济实惠的价格提供，包括往返运送费和在您现场使用 10 天的费用。 
4. 过程简单
    - {{site.data.keyword.IBM}} 向您发送预配置的设备，您只需连接并获取数据，然后将设备发回给 {{site.data.keyword.IBM}} 以将数据卸载到 {{site.data.keyword.cos_full}}。一旦数据卸载后，您可立即在云中访问这些数据，同时我们会以安全方式擦除设备。
5. 端到端保护
    - 设备设计使用 AES 256 位加密、RAID-6 配置以及防篡改、防水、防震的坚固机箱，从内到外最大限度地确保安全性，提高设备处理和传输过程中的数据保护和完整性。
6. 安全擦除
    - {{site.data.keyword.IBM}} 使用四遍 DOD 级别数据擦除来确保完全擦除 Mass Data Migration 设备中的所有客户数据。
    
    
<hr>


## Mass Data Migration 用例
1. 将数据迁移到云
    - 无论您是想释放内部部署存储空间、归档不活动数据还是备份数据以实现冗余和恢复，Mass Data Migration 都可以快速、安全地将您的数据移动到云中。

2. 数据中心退役
    - 在缩小数据中心大小、扩展数据中心或重新定位数据中心，快速启动数据中心变换，并使用 Mass Data Migration 将敏感数据安全地移至云中。

3. 有限带宽
    - 如果您处于偏远地区，或者发现通过网络进行数据传输的选项成本太高、速度太慢或无法使用，那么 Mass Data Migration 是一个很好的替代方法。
