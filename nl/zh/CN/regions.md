---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: region availability, storage locations, storage destinations

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

# 区域可用性
{: #regions}

通过 {{site.data.keyword.mdms_full}} 和 {{site.data.keyword.cos_full_notm}}，您可以从不同的存储选项中进行选择，以满足可用性和弹性需求。  
{: shortdesc}

## 支持的区域
{: #available-regions}

您可以在美国 (US)、欧盟 (EU)、日本、澳大利亚、巴西、新加坡、中国香港特别行政区、挪威、韩国、加拿大和墨西哥订购 {{site.data.keyword.mdms_short}} 设备。

订购设备之前，请记住以下装运和数据传输限制：

- **{{site.data.keyword.mdms_short}} 设备不能跨国际边境运送**（但欧盟及其 28 个成员国家/地区除外）。例如，不能将数据导入到一个区域中的设备中，然后将该设备运送到其他区域。
- **只能在源数据所在的国家/地区内传输数据**（但“欧盟跨区域”和“亚太地区跨区域”除外）。这意味着 Cloud Object Storage 存储区目标也必须位于 {{site.data.keyword.mdms_short}} 设备将在其中登台以进行数据卸载的数据中心所在的国家/地区。 

## 存储目标
{: #storage-destinations}

数据会迁移到 Cloud Object Storage 中，在其中可以针对存储的数据，从不同的存储类、位置和弹性中进行选择。 

{{site.data.keyword.mdms_short}} 支持可用于 Cloud Object Storage 的所有存储位置和弹性选项。下表将每个国家/地区与其可用数据中心和数据卸载选项相对应。

|国家/地区|数据中心|存储目标|
|-----|-----|----|
|巴西|圣保罗|单个站点：`sao01`|
|加拿大|蒙特利尔<br>多伦多|单个站点：`mon01`<br>单个站点：`tor01`|
|墨西哥|墨西哥城|单个站点：`mex01`|
|美国|达拉斯<br>圣何塞<br>华盛顿|跨区域：`us-geo`<br>区域：`us-south`<br>区域：`us-east`<br>单个站点：`sjc04`|
{: caption="表 1. 列出美洲的可用数据卸载位置" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

|国家/地区|数据中心|存储目标|
|-----|-----|----|
|德国|法兰克福|跨区域：`eu-geo`<br>区域：`eu-de`| 
|意大利|米兰|跨区域：`eu-geo`<br>单个站点：`mil01`| 
|荷兰|阿姆斯特丹|跨区域：`eu-geo`<br>单个站点：`ams03`| 
|挪威|奥斯陆|跨区域：`eu-geo`<br>单个站点：`oslo1`| 
|英国|伦敦|跨区域：`eu-geo`<br>区域：`eu-gb`|
{: caption="表 2. 列出欧洲的可用数据卸载位置" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

|国家/地区|数据中心|存储目标|
|-----|-----|----|
|澳大利亚|墨尔本<br>悉尼|跨区域：`ap-geo`<br>区域：`au-syd`<br>单个站点：`mel01`|
|中国香港特别行政区|中国香港特别行政区|跨区域：`ap-geo`<br>单个站点：`hkg02`|
|印度|金奈|跨区域：`ap-geo`<br>单个站点：`che01`| 
|日本|东京|跨区域：`ap-geo`<br>区域：`jp-tok`|
|韩国|首尔|跨区域：`ap-geo`<br>单个站点：`seo01`| 
|新加坡|新加坡|跨区域：`ap-geo`| 
{: caption="表 3. 列出亚太地区的可用数据卸载位置" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

有关存储区目标的更多信息，请参阅 [Cloud Object Storage 文档](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints)。
