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

# 地區可用性
{: #regions}

使用 {{site.data.keyword.mdms_full}} 和 {{site.data.keyword.cos_full_notm}}，您可以選擇不同的儲存空間選項，以符合可用性和備援需求。  
{: shortdesc}

## 支援的地區
{: #available-regions}

您可以在美國 (US)、歐盟 (EU)、日本、澳洲、巴西、新加坡、香港、挪威、南韓、加拿大及墨西哥訂購 {{site.data.keyword.mdms_short}} 裝置。

訂購裝置之前，請記住下列運送和資料傳送限制：

- **{{site.data.keyword.mdms_short}} 裝置不能跨國界運送**（歐盟和其 28 個成員國家除外）。例如，您無法將資料匯入至某個地區中的裝置，然後將該裝置運送到另一個地區。
- **您只能在來源資料所在國家/地區內傳送資料**（「歐盟跨地區」和「亞太地區跨地區」除外）。這表示，您的 Cloud Object Storage 儲存區目的地也必須與資料中心位於相同的國家/地區，而在資料中心內將暫置 {{site.data.keyword.mdms_short}} 裝置以進行資料卸載。 

## 儲存空間目的地 
{: #storage-destinations}

您的資料會移轉至 Cloud Object Storage，您可以在其中為已儲存的資料選擇不同的儲存空間類別、位置及備援。 

{{site.data.keyword.mdms_short}} 支援可用於 Cloud Object Storage 的所有儲存位置和備援選項。下表會將每個國家/地區對映至其可用的資料中心和資料卸載選項。

| 國家/地區 | 資料中心 | 儲存空間目的地 |
|-----|-----|----|
| 巴西 | 聖保羅 | 單一站台：`sao01`  |
| 加拿大 | 蒙特婁<br>多倫多 | 單一站台：`mon01` <br>單一站台：`tor01` |
| 墨西哥 | 墨西哥市 | 單一站台：`mex01` |
| 美國 | 達拉斯<br>聖荷西<br>華盛頓特區 | 跨地區：`us-geo`<br>地區：`us-south`<br>地區：`us-east`<br>單一站台：`sjc04` |
{: caption="表 1. 列出美洲可用的資料卸載位置" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| 國家/地區 | 資料中心 | 儲存空間目的地 |
|-----|-----|----|
| 德國 | 法蘭克福 | 跨地區：`eu-geo`<br>地區：`eu-de`  | 
| 義大利 | 米蘭 | 跨地區：`eu-geo`<br>單一站台：`mil01`  | 
| 荷蘭 | 阿姆斯特丹 | 跨地區：`eu-geo`<br>單一站台：`ams03`| 
| 挪威 | 奧斯陸 | 跨地區：`eu-geo`<br>單一站台：`oslo1`  | 
| 英國 | 倫敦 | 跨地區：`eu-geo`<br>地區：`eu-gb`  |
{: caption="表 2. 列出歐洲可用的資料卸載位置" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| 國家/地區 | 資料中心 | 儲存空間目的地 |
|-----|-----|----|
| 澳洲 | 墨爾本<br>雪梨 | 跨地區：`ap-geo`<br>地區：`au-syd`<br>單一站台：`mel01` |
| 香港 | 香港 | 跨地區：`ap-geo`<br>單一站台：`hkg02` |
| 印度 | 清奈 | 跨地區：`ap-geo`<br>單一站台：`che01` | 
| 日本 | 東京 | 跨地區：`ap-geo`<br>地區：`jp-tok` |
| 南韓 | 首爾 | 跨地區：`ap-geo`<br>單一站台：`seo01` | 
| 新加坡 | 新加坡 | 跨地區：`ap-geo`| 
{: caption="表 3. 列出亞太地區可用的資料卸載位置" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

如需儲存空間儲存區目的地的相關資訊，請參閱 [Cloud Object Storage 文件](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints)。
