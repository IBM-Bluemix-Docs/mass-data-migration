---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# 存取裝置使用者介面
{: #access-ui}

配置用於乙太網路連線的 {{site.data.keyword.mdms_full}} 裝置之後，您已準備好存取裝置使用者介面，讓您可以與裝置互動，並開始進行資料移轉處理程序。
{: shortdesc}

## 擷取裝置認證（測試版）
{: #retrieve-device-credentials}

當您提交 {{site.data.keyword.mdms_short}} 要求時，服務會代表您自動產生認證，您可以使用該認證來存取裝置的本端 Web 使用者介面。 

此特性是 [{{site.data.keyword.mdms_short}} 測試版](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)的一部分。您也可以從 [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} 的_要求詳細資料_ 區段中存取儲存裝置的認證。
{: note}

若要擷取裝置認證，請執行下列動作：

1. [登入 {{site.data.keyword.cloud_notm}} 主控台](https://{DomainName}/){: external}。
2. 移至**功能表** &gt; **資源清單**，以檢視資源清單。
3. 從 {{site.data.keyword.cloud_notm}} 資源清單中，選取您已佈建的 {{site.data.keyword.mdms_short}} 實例。
4. 在_要求詳細資料_ 標籤中，導覽至「認證」區段。
5. 複製**使用者名稱**和**密碼**值。

## 登入裝置使用者介面
{: #log-in-ui}

使用您在前一個步驟中所擷取的裝置認證來登入本端 Web 使用者介面，並與 {{site.data.keyword.mdms_short}} 裝置互動。

1. 開啟 Web 瀏覽器，並導覽至您在訂單表格中所提供的靜態 IP 位址。

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   將 `<device_management_IP_address>` 取代為針對 Eth1 或 Eth2 網路埠所配置的 IP 位址。接受憑證異常狀況。

2. 使用您在前一個步驟中所擷取的使用者名稱和密碼來登入裝置使用者介面。 

   ![「登入」頁面](images/login.png)
   
   即會顯示「一般作業」精靈。請由左至右使用各選項，以開始匯入資料。

   ![工作流程圖示](images/workflow.png)

   您可以使用介面左上角的**工作流程管理程式**，重新開啟「一般作業」精靈。
   {:tip}

## 後續步驟
{: #access-ui-next-steps}

- 若要準備資料汲取複製，請從[解除鎖定裝置上的儲存區](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool)開始。
