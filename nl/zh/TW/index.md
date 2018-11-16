---

copyright:
  years: 2017-2018
lastupdated: "2018-10-31"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# 開始使用 {{site.data.keyword.cloud_notm}} Mass Data Migration

**必要條件**

請先收集此資訊，再提交 Mass Data Migration 要求及完成移轉。

1. 儲存裝置的網路設定
   - 靜態 IP 位址
   - 啟用資料傳送的網路遮罩
2. 遠端電腦的網路設定
   - 靜態 IP 位址
   - 網路遮罩
   - 用來存取使用者介面的預設閘道
3. Cloud Object Storage 下載目的地 <br/>
   
   您在「美國標準跨地區」或「歐盟跨地區」必須至少具有一個 {{site.data.keyword.cos_full}} 帳戶及一個儲存區，才能完成要求表單。如果您還沒有 {{site.data.keyword.cos_full_notm}}} 帳戶，請在要求 Mass Data Migration 裝置之前先建立一個帳戶。請參閱[關於 {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}。
{:important}

## 建立要求

1. 使用您的唯一認證登入 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}。
2. 從「導覽列」中，選取**儲存空間** > **資料移轉** > **Mass Data Migration**，以存取 Mass Data Migration 登入頁面。
3. 按一下**要求裝置**，以開啟訂單表單。
4. 完成 **Mass Data Migration** 訂單表單中的每一個欄位。
   - **出貨地址** - 此表單並未預先填入，而且每個欄位都可編輯。請在「注意」欄位中提供將接受裝置交付之人員的名稱。挑選交付地點時，請考量裝置的重量（加上外殼有 66 磅）及可存取性。
   
   此裝置配備輪子及用於操作的彈出式把手。
   {:note}

   - **主要移轉聯絡人** - 此表單並未預先填入。每一個欄位都可編輯。可以新增多個人。
   - **資料中心網路配置** - 提供網路配置詳細資料，以在出貨前於 Mass Data Migration 裝置上預先佈建 Eth3 埠。
   - **資料卸載目的地** - 從清單中選取現有的目標帳戶。
   - **要求名稱** - 輸入名稱，以協助您追蹤訂單。
5. 在閱讀每份服務合約之後，請選取**我已閱讀並同意 Mass Data Migration 合約的完整條款**勾選框。
6. 按一下**工作區要求**，以提交「要求」。按一下**取消**，完全放棄表單並回到 Mass Data Migration 登入頁面。


## 準備及出貨

在您提交要求之後，要求問題單的狀態會呈現為`正在處理要求`。接受要求時，{{site.data.keyword.IBM}} 會開始預先配置下一台可用的裝置。

正在準備裝置時，[要求](https://control.softlayer.com/storage/mdms){:new_window}頁面上的狀態會顯示`正在準備裝置`，後面接著顯示`正在等待出貨`。「要求」進入`正在等待出貨` 狀態之後，就無法被取消。

當裝置由快遞接收並運送到您的地點時，「要求」狀態就會更新為`裝置已出貨`。會在[要求](https://control.softlayer.com/storage/mdms){:new_window}頁面的**訂單詳細資料**區段中與您分享追蹤號碼。


## 接收及連接

1. 會為您預先配置裝置。包括基本的[電源及連線指示](user-instructions.html)。<br/>
  
   使用者名稱及儲存區密碼會分開提供。檢查[要求](https://control.softlayer.com/storage/mdms){:new_window}中的**要求詳細資料**，以取得認證資訊。
   {:note}
2. 將瀏覽器指向您在訂單表單中提供的靜態 IP 位址。
3. 登入，並輸入密碼以解除鎖定空的儲存區。<br/>
   
   請參閱[要求](https://control.softlayer.com/storage/mdms){:new_window}頁面中的「要求詳細資料」，以取得密碼資訊。
   {:tip}
4. 在伺服器上裝載 NFS 共用。
5. 重新執行 DataShuttle 庫存，以確定擷取所有的新檔案。

## 移動資料
1. 執行 DataShuttle 複製，以移動資料。
2. 鎖定儲存區。
3. 溫和地關閉 Mass Data Migration 裝置。
4. 使用提供的出貨標籤，將盒子送回「{{site.data.keyword.BluSoftlayer_full}} 資料中心」。

當裝置回到 {{site.data.keyword.BluSoftlayer}} 時，要求狀態會變更為`已收到裝置`。

## 卸載並存取

在傳送過程期間，要求狀態顯示會顯示為`正在卸載資料`。移轉至 {{site.data.keyword.objectstorageshort}}「儲存區」完成時（`卸載完成`），狀態會再次變更。完成高速卸載至 Cloud Object Storage 儲存區時，您的資料便立即可供存取。

## 消除裝置

{{site.data.keyword.IBM}} 會實作 DOD 層級資料抹除需求，以永久清除裝置中的資料。完成時，「要求」狀態會顯示`清除完成`。
