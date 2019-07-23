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

# 關於 {{site.data.keyword.mdms_short}}
{: #about}

{{site.data.keyword.mdms_full}} 是一種快速、簡單且安全的方式，可實際將數 TB 到數 PB 的資料傳送至 {{site.data.keyword.cloud_notm}}。
{: shortdesc}

## 為何要使用 {{site.data.keyword.mdms_short}}？
{: #use-cases}

{{site.data.keyword.mdms_short}} 藉由提供可攜式且預先配置的儲存裝置來輕鬆移轉資料，以協助您簡化邁向雲端的旅程。在下列視訊中，您可以進一步瞭解 {{site.data.keyword.mdms_short}} 特性及使用案例。

<iframe class="embed-responsive-item" id="youtubeplayer" title="Mass Data Migration 提供快速、簡單且安全的方式，以將資料傳送至 IBM Cloud" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


|使用案例|說明|
| --- | --- |
|將資料移轉至雲端|無論您是要釋放內部部署儲存空間、保存非作用中資料，還是備份資料以供備援及回復使用，{{site.data.keyword.mdms_short}} 都可以快速且安全地將您的資料移至雲端。|
|資料中心解除任務|在縮小、擴展或重新定位資料中心時，快速啟動資料中心轉換並使用 {{site.data.keyword.mdms_short}} 將機密資料安全地移至雲端中。|
|限制頻寬|如果您處於偏遠的地點或發現網路選項成本過高、速度太慢或無法用於您的資料傳送，{{site.data.keyword.mdms_short}} 會是一個很好的選擇。|
{: caption="表 1. 說明 {{site.data.keyword.mdms_short}} 使用案例" caption-side="top"}

您可以藉由[探索資料移轉解決方案](https://www.ibm.com/cloud/data-migration)，來比較 {{site.data.keyword.cloud_notm}} 上的資料移轉選項。若要進一步瞭解 {{site.data.keyword.mdms_short}} 特性和好處，請查看 [{{site.data.keyword.mdms_short}} 產品頁面](https://www.ibm.com/cloud/mass-data-migration){: external}。
{: tip}

## 如何運作
{: #how-it-works}

{{site.data.keyword.mdms_short}} 使用 120 TB 可用容量的儲存裝置加速將資料移動至雲端，並克服常見的傳送難題，例如高成本、冗長的傳送時間及安全疑慮。

下圖說明 {{site.data.keyword.mdms_short}} 處理程序。

![說明 Mass Data Migration 處理程序。](images/mdms-workflow.png){: caption="圖 1. 說明 Mass Data Migration 工作流程。" caption-side="bottom"}

## 服務元件
{: #service-componenets}

{{site.data.keyword.mdms_short}} 包含下列服務元件。

<dl>
   <dt>{{site.data.keyword.mdms_short}} 儀表板</dt>
      <dd>您可以從 <a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a> 的服務儀表板中，建立及追蹤 {{site.data.keyword.mdms_short}} 訂單。在 {{site.data.keyword.mdms_short}} 要求頁面中，您可以指定裝置的網路配置設定、擷取認證來登入裝置，以及追蹤訂單狀態。</dd>
   <dt>{{site.data.keyword.mdms_short}} 裝置</dt>
      <dd>{{site.data.keyword.mdms_short}} 提供運送到您位置的<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">可攜式儲存裝置</a>。{{site.data.keyword.mdms_short}} 裝置在送達時已預先配置，並準備好連接至您的網路。</dd>
   <dt>裝置使用者介面</dt>
      <dd><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">裝置使用者介面</a>是本端 Web 型使用者介面，您可以用來存取 {{site.data.keyword.mdms_short}} 裝置上的網路共用。該使用者介面的基礎是成熟的檔案及網路軟體，可以將大量的大型檔案複製並傳輸到 {{site.data.keyword.cloud_notm}}。</dd>
</dl>










