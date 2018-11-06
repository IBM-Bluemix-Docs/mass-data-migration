---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# {{site.data.keyword.cloud_notm}} Mass Data Migration 常見問題

## Q1. 何謂 {{site.data.keyword.cloud_notm}} Mass Data Migration？ 
{{site.data.keyword.cloud}} Mass Data Migration 是一項實體資料傳送服務，使用堅固的 120 TB 可用容量可攜式儲存裝置，將 TB 到 PB 的資料安全移動到 {{site.data.keyword.cloud_notm}}。 

## Q2. 如何開始使用 Mass Data Migration？ 
使用 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 來提交要求。在要求被核准且進行處理之後，下一台（或多台）可用的裝置將預先配置，並根據您的網路及出貨資訊出貨給您。使用下列鏈結立即啟動：https://control.softlayer.com/storage/mdms

## Q3. Mass Data Migration 的適用對象？ 
Mass Data Migration 裝置可在幾乎任何環境中執行，從資料中心和辦公室到偏遠的地點、倉庫和船隻。如果網路資料傳送選項成本過高、速度太慢或無法使用，則 Mass Data Migration 也是一種選擇。  

## Q4. 使用 Mass Data Migration 可以傳送的資料量？
對於您可以傳送的資料量幾乎沒有限制，無論是幾 TB 還是幾 PB。每一台裝置在 RAID-6 上最多可保留 120 TB 的可用容量，但您可以使用多台裝置來容納更大的工作負載。

## Q5. 如何使用多台裝置來移動超過 120 TB 的較大工作負載？ 
並行或串聯使用多台裝置來移動單一移轉中的所有資料，或者在反覆運算移轉中使用單一裝置。例如，並行使用 9 台裝置傳送 1 PB 資料，或在 9 次個別移轉中使用單一裝置。

## Q6. 傳送資料需要多久的時間？ 
從客戶提交「Mass Data Migration 要求」到可在客戶的 {{site.data.keyword.cos_full}} 儲存區中存取其資料的時間，處理時間最短只要 7 天。

## Q7. 可以擁有 Mass Data Migration 裝置多久？  
在前 10 個營業日內，裝置可免費保留在站上。這不包括裝置的出貨日或收貨日。如果需要更多時間才能完成汲取，您可以延長您的使用時間，之後為每天 30 美元（適用於美國和歐盟地區）。 

## Q8. Mass Data Migration 支援的網路介面？  
Mass Data Migration 裝置具備 10 Gbps 網路介面，其中包含 RJ45 (CAT6a) & SFP+ 銅線（包括 RJ45 到 SFP+ 轉換器）網路埠。

## Q9. 何謂 Mass Data Migration 預設出貨選項？ 
Mass Data Migration 使用 UPS Next Day Air 往返遞送來運送所有裝置。此成本包括在每台裝置 395 美元的低廉固定費用中。客戶目前無法選取其他出貨方式。

## Q10. Mass Data Migration 可用地區？ 
Mass Data Migration 只能在美國及歐盟使用。所有資料都會分別移轉至服務的美國標準跨區域或歐盟跨區域層級中的 {{site.data.keyword.cos_full}}。裝置不得從甲地出貨，但運回乙地。

## Q11. 將資料匯入至 {{site.data.keyword.cloud_notm}} 需要多少成本？ 
將資料傳送至 {{site.data.keyword.cloud_notm}} 不會產生任何費用。

## Q12. 我可以使用 Mass Data Migration 從 {{site.data.keyword.cloud_notm}} 中匯出資料嗎？ 
Mass Data Migration 目前不支援將資料匯出 {{site.data.keyword.cloud_notm}}。

## Q13. Mass Data Migration 會將資料加密嗎？ 
Mass Data Migration 會使用 AES 256 位元加密來加密所有資料，並提供一個高保護性密碼來解除鎖定儲存區。{{site.data.keyword.IBM}} 內的所有資料傳送都是透過 SSL 完成的。

## Q14. Mass Data Migration 如何實際保護資料的安全？ 
所有 Mass Data Migration 裝置都存放在堅固耐用的機殼中。這些外殼具有防水、防震及防竄改功能，可確保往返裝置及資料安全。 

## Q15. 如何在整個移轉過程中追蹤我的要求？ 
若要追蹤「要求」的狀態，請參閱 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中 Mass Data Migration 頁面上的作用中要求區段。您可以使用下列鏈結登入入口網站：https://control.softlayer.com/storage/mdms

## Q16. 在將裝置卸載至 {{site.data.keyword.cos_full_notm}} 之後，如何從裝置中清除資料？
只要資料卸載至 {{site.data.keyword.cos_full}} 已完成，{{site.data.keyword.IBM}} 就會立即啟動 4 次的 DOD 層級資料抹除，以永久清除裝置中的資料。 

## Q17. Mass Data Migration 上的檔案介面為何？ 
Mass Data Migration 使用「網路檔案系統 (NFS)」。

## Q18. 如何在 Mass Data Migration 上使用檔案介面？ 
解除鎖定加密儲存區之後，在包含要移轉的資料的伺服器上裝載 NFS 共用，然後開始將資料檔案複製到 NFS 共用中。

## Q19. Mass Data Migration 上的檔案介面的好處為何？ 
該檔案介面的基礎是成熟的檔案及網路軟體，可以將大量的大型檔案複製並傳輸到 {{site.data.keyword.cloud_notm}}。

## Q20. 如何將檔案儲存在 Mass Data Migration 裝置上？ 
Mass Data Migration 裝置使用含有 LZ4 壓縮及 AES 256 位元加密的 ZFS 檔案系統。

## Q21. 在美國使用 Mass Data Migration 需要多少成本？ 
在美國，每台裝置收取 395 美元的固定費用，包括 295 美元的裝置費用，100 美元的往返 UPS Next Day Air 遞送，以及現場使用 10 個營業日。 

## Q22. 是否會向我收取 {{site.data.keyword.cos_full_notm}} 的使用費？ 
將資料傳送到 {{site.data.keyword.cloud_notm}} 是免費的，不過，標準費率會套用於儲存在 {{site.data.keyword.cos_full}} 或任何其他 {{site.data.keyword.cloud_notm}} 服務中的資料。您可以在下列鏈結中找到標準跨區域產品與服務的 {{site.data.keyword.cos_full}} 的定價：https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## Q23. 我可以購買 {{site.data.keyword.cloud_notm}} Mass Data Migration 裝置嗎？ 
{{site.data.keyword.cloud_notm}} Mass Data Migration 裝置不提供購買。 
