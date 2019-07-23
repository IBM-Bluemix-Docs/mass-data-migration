---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# 解除鎖定儲存區
{: #unlock-storage-pool}

您可以先解除鎖定並啟動針對裝置所佈建的儲存區，以將資料複製到 {{site.data.keyword.mdms_full}} 裝置。
{: shortdesc}

## 擷取儲存區通行詞組（測試版）
{: #retrieve-storage-pool-passcode}

若要存取 {{site.data.keyword.mdms_short}} 裝置上的儲存區，請導覽至 {{site.data.keyword.cloud_notm}} 主控台中的 {{site.data.keyword.mdms_short}} 要求詳細資料來擷取裝置認證。

此特性是 [{{site.data.keyword.mdms_short}} 測試版](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)的一部分。您也可以從 [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} 的_要求詳細資料_ 區段中存取儲存裝置的認證。
{: note}

若要擷取儲存區通行詞組，請執行下列動作：

1. [登入 {{site.data.keyword.cloud_notm}} 主控台](https://{DomainName}/){: external}。
2. 移至**功能表** &gt; **資源清單**，以檢視資源清單。
3. 從 {{site.data.keyword.cloud_notm}} 資源清單中，選取您已佈建的 {{site.data.keyword.mdms_short}} 實例。
4. 在_要求詳細資料_ 標籤中，導覽至「認證」區段。
5. 複製**儲存區鎖定密碼**值。

## 啟動儲存區
{: #activate-storage-pool}

使用您在前一個步驟中所擷取的認證，來解除鎖定空的儲存區。

1. [登入裝置使用者介面](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 在「一般作業」精靈中，按一下**解除鎖定並啟動儲存區**。
3. 輸入您在步驟 1 中所擷取的儲存區通行詞組，然後按一下**確定**。
      
   ![啟動儲存區](/images/StartStoragePool.png)

   依預設，共用同時啟用「網路檔案系統 (NFS)」和「伺服器訊息區塊 (SMB)」通訊協定，並且沒有存取限制。您可以在使用者介面中的共用名稱上按一下滑鼠右鍵，然後選取適當的功能表選項，來修改對 NFS 或 SMB 的這個共用的存取權。
   {: note}

## 後續步驟
{: #unlock-storage-pool-next-steps}

- 如果您使用 Unix 機器，請[使用 NFS 來連接網路共用](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share)。
- 如果您使用 Windows 機器，請[使用 SMB 來連接至網路共用](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share)。
- 啟動[資料複製處理程序](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy)。
