---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# 驗證資料
{: #verify-data}

您可以使用 {{site.data.keyword.cos_full}} 來存取及驗證已移轉的資料。
{: shortdesc}

卸載完成之後，在 {{site.data.keyword.cloud_notm}} 安全地清除裝置的同時，立即存取雲端中的資料。

## 存取 Cloud Object Storage 中的資料
{: #access-data-cos}

您可以在提交 {{site.data.keyword.mdms_short}} 要求時所指定的 Cloud Object Storage 實例中，使用您的已移轉資料。刪除來源伺服器中的資料之前，請確認已將資料順利上傳至 {{site.data.keyword.cloud_notm}}。

若要存取及驗證資料，請執行下列動作： 

1. [登入 {{site.data.keyword.cloud_notm}} 主控台](https://{DomainName}/){: external}。
2. 移至**功能表** &gt; **資源清單**，以檢視資源清單。
3. 從 {{site.data.keyword.cloud_notm}} 資源清單中，選取您已佈建的 Cloud Object Storage 實例。
4. 從可用的儲存空間儲存區清單中，選取您為資料移轉所指定的儲存區名稱。
5. 確認與儲存區相關聯的物件符合您複製到 {{site.data.keyword.mdms_short}} 裝置的資料。

## 將資料移至不同的儲存空間解決方案
{: #move-data}

取決於工作負載需求，您可能需要將移轉的資料從 Cloud Object Storage 移至不同的雲端儲存空間解決方案（例如 [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) 或 [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage)）。 

若要進一步瞭解儲存空間移轉選項，請查看[秘訣：將資料從 COS 移至 File 或 Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}。

