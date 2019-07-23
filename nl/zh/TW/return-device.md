---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# 送回裝置
{: #return-device}

關閉電源，並將 {{site.data.keyword.mdms_full}} 裝置送回至 {{site.data.keyword.cloud_notm}}，以完成移轉處理程序。
{: shortdesc}

## 中斷裝置的連線
{: #disconnect-device}

資料複製處理程序完成時，您可以溫和地關閉系統電源。

1. 在「一般作業」精靈中，按一下**關閉應用裝置**。

    ![關閉應用裝置](images/ShutDown.png)

    按一下**確定**，以確認。
2. 使用裝置上的**系統開啟/關閉**按鈕，來關閉裝置電源。 
3. 將**主開關**設為**關閉**。
4. 整理所有纜線和光學設備，並將它們放回運輸箱內的儲存位置。

## 將裝置運送至 {{site.data.keyword.cloud_notm}}
{: #ship-device}

備妥運送標籤，並在準備好送回裝置時通知您的快遞。

1. 擷取裝置的庫存清單和送回運送標籤。這些文件位於運輸箱蓋下方。

    如果您要運送多台裝置，請記住，每個箱子中所提供的送回運送標籤都是儲存裝置所特有。在您向快遞排定取貨之前，請確定將對應的送回運送標籤貼在適當的裝置上。
    {: note}
2. 使用庫存清單來確認所有纜線和光學設備都已送回並儲存在運輸箱中。
3. 將庫存清單放回運輸箱，然後使用送回運送標籤上所列出的指示，將標籤貼在裝置上。
4. 向快遞排定取貨，然後將裝置送回資料中心。

    當裝置回到 {{site.data.keyword.cloud_notm}} 時，在 {{site.data.keyword.mdms_short}} 要求詳細資料頁面中，訂單狀態會變更為_已收到裝置_。

## 後續步驟
{: #return-device-next-steps}

- [管理 {{site.data.keyword.mdms_short}} 要求](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)，以檢查訂單狀態。
- 刪除來源伺服器中的資料之前，請[確認已將資料順利上傳至 {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data)。

