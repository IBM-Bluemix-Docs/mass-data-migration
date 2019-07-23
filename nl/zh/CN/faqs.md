---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# 常见问题
{: #faqs}

有关 {{site.data.keyword.mdms_full}} 的常见问题。
{: shortdesc}

## 什么是 {{site.data.keyword.mdms_full_notm}}？
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} 是一种物理数据传输服务，使用可用容量为 120 TB 的坚固便携式存储设备，将太字节到拍字节数量级的数据更快地安全移动到 {{site.data.keyword.cloud_notm}}。

## 如何开始使用 {{site.data.keyword.mdms_short}}？
{: #how-to-use-mdms}
{: faq}

使用 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} 提交请求。您的请求获得批准并经过处理后，将对接下来的一个或多个可用设备进行配置，然后根据您的网络和发货信息发送给您。 

## 谁应该使用 {{site.data.keyword.mdms_short}}？
{: #who-uses-mdms}
{: faq}

{{site.data.keyword.mdms_short}} 设备配备为几乎可以在任何环境中运行，从数据中心和办公室一直到远程位置（例如，石油钻塔和船舶）。此外，如果通过网络传输数据的选项的成本高得离谱、速度太慢或不可用，那么 {{site.data.keyword.mdms_short}} 也可作为一种非常不错的替代方法。

## 使用 {{site.data.keyword.mdms_short}} 可以传输多少数据？
{: #how-much-data}
{: faq}

您可以传输的数据量几乎没有限制，不管是只有几个太字节的数据还是有许多拍字节的数据。每个设备最多可容纳 120 TB 可用容量（RAID-6 配置），但您可以使用多个设备来容纳更大的工作负载。{{site.data.keyword.mdms_short}} 还提供了内联压缩功能，这可进一步提高可用容量，具体取决于数据集的可压缩程度。最大的单个对象大小限制为 10 TB。


## 如何使用多个设备来移动超过 120 TB 的更大型工作负载？
{: #using-multiple-devices}
{: faq}

并行或串行使用多个设备可在单个迁移中移动所有数据，也可以使用单个设备进行迭代迁移。例如，并行使用 9 个设备来传输 1 PB 数据，或者使用单个设备进行 9 次单独的迁移。如果并行使用多个设备，请记住数据获取速率会变慢。

## 传输数据需要多长时间？
{: #transfer-timeline}
{: faq}

从客户提交 {{site.data.keyword.mdms_short}} 请求到其数据在 IBM Cloud Object Storage 存储区中可访问，这整个周转时间可能需要好几天。传输性能可能会受到许多因素（例如，联网、带宽或要传输的文件数）的影响。例如，传输数百万个小文件所用的时间要长于传输数量相对较少但更大的文件中包含的相同数据量。

## 我可以保留 {{site.data.keyword.mdms_short}} 设备多长时间？
{: #device-onsite-time}
{: faq}

设备可在现场免费保留前 10 个工作日。这不包括设备发货日期，也不包括设备返还给 IBM 的日期（最多 2 天）。如果需要更长时间来完成数据获取，可以延长使用时间，但延长的时间会按每个日历天 30 美元收费。这适用于所有区域。

## {{site.data.keyword.mdms_short}} 支持哪些网络接口？
{: #supported-network-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} 设备具有带 RJ45 (CAT6a) 和 SFP+ 铜缆网络端口的 10 Gbps 网络接口。

RJ45 到 SFP+ 转换器仅在缺少 SFP+ 本机连接的设备型号中随附。目前不支持光纤。

## {{site.data.keyword.mdms_short}} 的缺省发货选项是什么？
{: #shipping-options}
{: faq}

{{site.data.keyword.mdms_short}} 使用 UPS 次日达航空往返速递来运送所有设备。成本含在每个设备 395 美元的低廉统一费率中。客户当前无法选择其他发货方式。


## 哪些区域提供 {{site.data.keyword.mdms_short}}？
{: #regions-available}
{: faq}

目前，{{site.data.keyword.mdms_short}} 在美国 (US)、欧盟 (EU)、日本、澳大利亚、巴西、新加坡、中国香港特别行政区、挪威、韩国、加拿大和墨西哥提供。后续将扩展到其他地理区域。在线订购在大多数区域中可用。对于不支持在线订购的任何区域，请联系 IBM 销售代表以询问关于使用该服务的信息。

设备不能跨国际边境运送（例如，不能在一个区域中订购设备，然后将该设备运送到其他区域），但欧盟及其 28 个成员国家/地区除外。
{: note}

## {{site.data.keyword.mdms_short}} 在美国的缺省发货选项是什么？
{: #default-shipping-us}
{: faq}

对于美国设备，{{site.data.keyword.mdms_short}} 使用 UPS 往返隔日运送。运费包含在价格中。客户当前无法选择替代装运方法。 

## {{site.data.keyword.mdms_short}} 在欧盟的缺省发货选项是什么？
{: #default-shipping-eu}
{: faq}

对于欧盟设备，{{site.data.keyword.mdms_short}} 使用 FedEx 往返隔日运送。运费包含在价格中。客户当前无法选择替代装运方法。 

## {{site.data.keyword.mdms_short}} 在其他所有受支持区域的缺省发货选项是什么？
{: #default-shipping-other}
{: faq}

对于美国和欧盟以外的所有受支持区域，运送供应商和运送周转时间将有所不同。运费包含在价格中。客户当前无法选择替代装运方法。

在这些区域中，IBM 无法在您下订单时预订往返运送，而是在需要装运时预订单向运送。对于出库装运，请至少给 IBM 留出三个工作日，以便在您提交请求后协调 {{site.data.keyword.mdms_short}} 设备装运。
{: note}

对于非美国和非欧盟订单，请在所需的设备发货日期之前，至少提前三个工作日请求该设备的返还装运。例如，如果要在周五装运设备，请在同一周的周一协调返还装运。您可以在 {{site.data.keyword.mdms_short}} 仪表板中的_请求详细信息_选项卡中请求返还装运。
{: important}

## 我在日本、澳大利亚、巴西、加拿大、墨西哥、中国香港特别行政区、新加坡、挪威或韩国。如何请求 {{site.data.keyword.mdms_short}} 设备的返还装运？
{: #shipping-timetable-other}
{: faq}

如果是在美国和欧盟区域之外使用 {{site.data.keyword.mdms_short}}，那么需要在所需的设备发货日期之前，至少提前三个工作日请求该设备的返还装运。例如，如果要在周五装运设备，请在同一周的周一协调返还装运。

## 将数据导入到 {{site.data.keyword.cloud_notm}} 的成本是多少？
{: #data-transfer-cost}
{: faq}

将数据传输到 {{site.data.keyword.cloud_notm}} 中不会产生费用。


## 可以使用 {{site.data.keyword.mdms_short}} 从 {{site.data.keyword.cloud_notm}} 导出数据吗？
{: #exporting-data}
{: faq}

目前，{{site.data.keyword.mdms_short}} 不支持从 {{site.data.keyword.cloud_notm}} 导出数据。


## {{site.data.keyword.mdms_short}} 会加密数据吗？
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}} 使用 AES 256 位加密技术来加密所有数据，并提供高强度密码来解锁存储池。{{site.data.keyword.IBM}} 中的所有数据传输均通过 SSL 完成。

## {{site.data.keyword.mdms_short}} 如何以物理方式保护数据安全？
{: #security}
{: faq}

所有 {{site.data.keyword.mdms_short}} 设备都安装在坚固耐用的机箱中。这些机箱具有防水、防震和防篡改功能，可确保往返途中设备和数据的安全。

## 如何在整个迁移过程中跟踪请求？
{: #how-to-track-request}
{: faq}

要跟踪请求的状态，请导航至 {{site.data.keyword.cloud_notm}} 控制台中 {{site.data.keyword.mdms_short}} 仪表板上的_请求详细信息_选项卡。

## 在 {{site.data.keyword.mdms_short}} 设备卸载到 {{site.data.keyword.cos_full_notm}} 之后，如何从设备中擦除数据？
{: #data-erasure}
{: faq}

数据卸载到 IBM Cloud Object Storage 完成后，IBM 会立即使用 NIST 数据擦除标准来擦除设备，以确保完全擦除设备中的所有客户数据。

## {{site.data.keyword.mdms_short}} 上的文件接口是什么？
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} 支持网络文件系统 (NFS) 和服务器消息块 (SMB) 协议。

## 如何使用 {{site.data.keyword.mdms_short}} 上的文件接口？
{: #how-to-use-file-interface}
{: faq}

首先，解锁加密池。然后，在包含要迁移的数据的服务器上安装共享。接着，就可以开始将数据文件复制到网络共享。

## {{site.data.keyword.mdms_short}} 上的文件接口有哪些优点？
{: #file-interface-benefits}
{: faq}

该文件接口基于成熟的文件和网络软件，可以将大量大型文件复制并传输到 {{site.data.keyword.cloud_notm}}。

## 如何在 {{site.data.keyword.mdms_short}} 设备上存储文件？
{: #file-storage}
{: faq}

{{site.data.keyword.mdms_short}} 设备使用采用 LZ4 压缩和 AES 256 位加密的 ZFS 文件系统。

## 在美国使用 {{site.data.keyword.mdms_short}} 需要多少成本？
{: #pricing-us}
{: faq}

在美国，按每台设备 395 美元的统一费率收费，其中包含 295 美元设备费、100 美元 UPS 往返隔日运送费和 10 个工作日在贵方现场的使用费。

现场使用 10 天不包括设备发货日期，也不包括设备返还给 IBM 的日期（最多 2 天）。如果需要更长时间来完成迁移，超过分配的 10 个工作日，那么每多使用一天，会按每天 30 美元收取延期费。

## 在欧盟使用 {{site.data.keyword.mdms_short}} 需要多少成本？
{: #pricing-eu}
{: faq}

在欧盟，按每台设备 445 美元的统一费率收费，其中包含 295 美元设备费、150 美元 FedEx 往返隔日运送费和 10 个工作日在贵方现场的使用费。

现场使用 10 天不包括设备发货日期，也不包括设备返还给 IBM 的日期（最多 2 天）。如果需要更长时间来完成迁移，超过分配的 10 天，那么每多使用一天，会按每天 30 美元收取延期费。

## 在其他所有受支持区域使用 {{site.data.keyword.mdms_short}} 需要多少成本？
{: #pricing-other}
{: faq}

在其他所有区域（日本、澳大利亚、巴西、加拿大、墨西哥、中国香港特别行政区、新加坡、挪威和韩国），按每台设备 1,145 美元的统一费率收费，其中包含 295 美元设备费、850 美元往返运送费和 10 个工作日在贵方现场的使用费。

现场使用 10 天不包括设备发货日期，也不包括设备返还给 IBM 的日期（最多 2 天）。如果需要更长时间来完成迁移，超过分配的 10 天，那么每多使用一天，会按每天 30 美元收取延期费。

对于这些区域，有特殊的装运需求。有关更多信息，请参阅前文中的内容。
{: note}

## 使用 {{site.data.keyword.cos_full_notm}} 会收取费用吗？
{: #pricing-cos}
{: faq}

将数据传输到 {{site.data.keyword.cloud_notm}} 是免费的。但是，标准费率适用于存储在 {{site.data.keyword.cos_full_notm}} 或其他任何 {{site.data.keyword.cloud_notm}} 服务中的数据。要了解有关 Cloud Object Storage 中定价选项的更多信息，请参阅 [{{site.data.keyword.cos_full_notm}} 定价](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}。 

## 可以购买 {{site.data.keyword.mdms_full_notm}} 设备吗？
{: #purchasing-devices}
{: faq}

{{site.data.keyword.mdms_full_notm}} 设备不可购买。

## {{site.data.keyword.mdms_short}} 进程如何保持对象名称的唯一性？
{: #object-name-uniqueness}
{: faq}

为了确保在将对象名称复制到 Cloud Object Storage 存储区时这些名称唯一，文件路径会在对象名称中包含一个前缀。例如，将 `/root/user/config.ini` 复制到存储区时，此路径会变为 `root/user/config.ini`。

## 如果 {{site.data.keyword.cos_full_notm}} 帐户中不存在目标存储区，会发生什么情况？
{: #target-buckets}
{: faq}

如果目标存储区不存在，请进行创建。如果确实存在，那么该存储区必须为空，否则无法继续复制。  

## 在扫描过程中会跳过链接吗？
{: #links-scan-process}
{: faq}

对。在扫描过程中会跳过符号链接和硬链接。
