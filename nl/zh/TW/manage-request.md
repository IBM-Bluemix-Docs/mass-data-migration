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

# 管理要求
{: #manage-request}

使用 {{site.data.keyword.slportal}} 來管理及追蹤 {{site.data.keyword.mdms_full}} 訂單的狀態。
{: shortdesc}

參與 {{site.data.keyword.mdms_short}} 測試版計畫，即可預覽能從 {{site.data.keyword.cloud_notm}} 主控台存取的新 {{site.data.keyword.mdms_short}} 服務儀表板。若要瞭解更多相關資訊，請參閱[取得測試版的存取權](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)。
{: tip}

## 追蹤訂單 
{: #track-order}

要求儲存裝置之後，您可以使用可從 {{site.data.keyword.slportal}} 取得的 [{{site.data.keyword.mdms_short}} 要求詳細資料頁面](https://control.softlayer.com/storage/mdms){: external}來追蹤訂單的進度。

下表顯示訂單狀態在 {{site.data.keyword.mdms_short}} 處理要求時的變更。

| 狀態 | 說明 |
| --- | --- |
| 正在處理要求 | {{site.data.keyword.mdms_short}} 收到要求之後，狀態會變更為_正在處理要求_。|
| 正在準備裝置 | 核准訂單之後，要求狀態會變更為_正在準備裝置_。{{site.data.keyword.mdms_short}} 會準備並配置下一個可用的儲存裝置。|
| 正在等待裝運 | 預先配置的儲存裝置正在等待裝運到您的位置。在要求進入_正在等待裝運_ 狀態之後，就無法再取消訂單。|
| 裝置已運送 | 儲存裝置已由快遞接收並運送到您的位置。您可以在[要求詳細資料頁面](https://control.softlayer.com/storage/mdms){: external}的_訂單詳細資料_ 區段中檢視追蹤號碼。|
| 已收到裝置 | 在裝置回到 {{site.data.keyword.cloud_notm}} 之後，狀態會變更為_已收到裝置_。|
| 正在卸載資料 | 在資料傳送過程中，要求狀態會變更為_正在卸載資料_。裝置會連接至 {{site.data.keyword.cloud_notm}} 資料中心內的網路，而且會自動啟動資料卸載。|
| 卸載完成 | 當卸載程序完成時，要求狀態會變更為_卸載完成_。現在，您可以在起始要求中指定的 Cloud Object Storage 目的地中使用您的資料。|
| 消除完成 | {{site.data.keyword.mdms_short}} 會使用 NIST 資料抹除標準永久地消除裝置中的資料。資料消除處理程序完成之後，訂單狀態會變更為_消除完成_。
{: caption="表 1. 說明 {{site.data.keyword.mdms_short}} 訂單狀態工作流程" caption-side="top"}
