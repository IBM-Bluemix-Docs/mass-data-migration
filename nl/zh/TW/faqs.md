---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# 常見問題
{: #faqs}

{{site.data.keyword.mdms_full}} 的常見問題。
{: shortdesc}

## 何謂 {{site.data.keyword.mdms_full_notm}}？
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} 是一項實體資料傳送服務，使用堅固的 120 TB 可用容量可攜式儲存裝置，加速將 TB 到 PB 的資料安全移動到 {{site.data.keyword.cloud_notm}}。

## 如何開始使用 {{site.data.keyword.mdms_short}}？
{: #how-to-use-mdms}
{: faq}

使用 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} 來提交要求。核准並處理要求之後，會配置下一台或多台可用的裝置，並根據您的網路及出貨資訊傳送給您。 

## 誰應該使用 {{site.data.keyword.mdms_short}}？
{: #who-uses-mdms}
{: faq}

從資料中心和辦公室到油井設備和船舶這類遠端位置，{{site.data.keyword.mdms_short}} 裝置幾乎可以在任何環境中執行。如果網路資料傳送選項成本過高、速度太慢或無法使用，則 {{site.data.keyword.mdms_short}} 也是一個很好的選擇。

## 使用 {{site.data.keyword.mdms_short}} 可以傳送多少資料？
{: #how-much-data}
{: faq}

對於您可以傳送的資料量幾乎沒有限制，無論是幾 TB 還是很多 PB。每一台裝置在 RAID-6 上最多可保留 120 TB 的可用容量，但您可以使用多台裝置來容納更大的工作負載。{{site.data.keyword.mdms_short}} 也提供行內壓縮，進一步根據資料集的可壓縮程度來增加可用容量。最大單一物件的大小限制為 10 TB。


## 如何使用多台裝置來移動超出 120 TB 的大量工作負載？
{: #using-multiple-devices}
{: faq}

並行或串聯使用多台裝置來移動單一移轉中的所有資料，或者在反覆運算移轉中使用單一裝置。例如，並行使用 9 台裝置傳送 1 PB 資料，或在 9 次個別移轉中使用單一裝置。如果您平行使用多台裝置，請記住，汲取率會較慢。

## 傳送資料需要多久的時間？
{: #transfer-timeline}
{: faq}

從客戶提交 {{site.data.keyword.mdms_short}} 要求到可在客戶的 IBM Cloud Object Storage 儲存區中存取其資料的時間，處理時間只要幾天。傳送效能可能會受到許多因素（如網路、頻寬或傳送的檔案數目）的影響。例如，相對於較少但較大檔案所包含的相同資料量，傳送數百萬個小型檔案所需的時間會較長。

## 我有多長時間可以使用 {{site.data.keyword.mdms_short}}？
{: #device-onsite-time}
{: faq}

在前 10 個營業日內，裝置可以保留在站上，不需額外費用。這不包括將裝置運送給您的那天，也不包括您將裝置送回 IBM 的那天（最多 2 天）。如果需要額外時間才能完成汲取，您可以延長使用時間，之後為每個行事曆日期 30 美元。適用於所有地區。

## {{site.data.keyword.mdms_short}} 支援的網路介面？
{: #supported-network-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} 裝置具備 10 Gbps 網路介面，其中包含 RJ45 (CAT6a) 和 SFP+ 銅纜網路埠。

RJ45 到 SFP+ 的轉換器只隨附於缺少 SFP+ 原生連線的裝置型號。目前不支援光纖。

## 何謂 {{site.data.keyword.mdms_short}} 預設運送選項？
{: #shipping-options}
{: faq}

{{site.data.keyword.mdms_short}} 使用 UPS Next Day Air 往返遞送來運送所有裝置。此成本包括在每台裝置 395 美元的低廉固定費用中。客戶目前無法選取其他出貨方式。


## {{site.data.keyword.mdms_short}} 可用地區？
{: #regions-available}
{: faq}

目前，美國 (US)、歐盟 (EU)、日本、澳洲、巴西、新加坡、香港、挪威、南韓、加拿大及墨西哥都有提供 {{site.data.keyword.mdms_short}}。正在進行其他地理區域的擴充。大部分地區都提供線上訂購。對於任何沒有線上訂購的地區，請與「IBM 業務代表」聯絡，以查詢如何使用此服務。

裝置不能跨國界運送（例如，不能在某個地區訂購裝置，但將裝置運送至另一個地區），但歐盟和其 28 個成員國家除外。
{: note}

## 美國的 {{site.data.keyword.mdms_short}} 預設運送選項為何？
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}} 針對美國裝置使用往返 UPS 隔日運送。運送成本已內含在價格中。客戶目前無法選取其他運送方式。 

## 歐盟的 {{site.data.keyword.mdms_short}} 預設運送選項為何？
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}} 針對歐盟裝置使用往返 FedEx 隔日運送。運送成本已內含在價格中。客戶目前無法選取其他運送方式。 

## 所有其他支援地區的 {{site.data.keyword.mdms_short}} 預設運送選項為何？
{: #default-shipping-other}
{: faq}

對於美國和歐盟以外的所有支援地區，運送供應商和運送處理時間將有所不同。運送成本已內含在價格中。客戶目前無法選取其他運送方式。

在這些地區中，IBM 無法在您下訂單時預訂往返運送。相反地，在需要裝運時，會預訂單程運送。對於出貨裝運，請至少讓 IBM 在您發出要求之後有三個營業日可以協調 {{site.data.keyword.mdms_short}} 裝置的裝運。
{: note}

對於非美國及非歐盟訂單，要求裝置的送回裝運至少在您要運送裝置的日期之前的三個營業日。例如，如果您要在星期五運送裝置，則請在同一週的星期一協調送回裝運。您可以在 {{site.data.keyword.mdms_short}} 儀表板的_要求詳細資料_ 標籤中，要求送回裝運。
{: important}

## 我位在日本、澳洲、巴西、加拿大、墨西哥、香港、新加坡、挪威或南韓。如何要求 {{site.data.keyword.mdms_short}} 裝置的送回運送？
{: #shipping-timetable-other}
{: faq}

如果您是在美國和歐盟以外的地區使用 {{site.data.keyword.mdms_short}}，則需要要求裝置的送回裝運至少在您要運送裝置的日期之前的三個營業日。例如，如果您要在星期五運送裝置，則請在同一週的星期一協調送回裝運。

## 將資料匯入至 {{site.data.keyword.cloud_notm}} 需要多少成本？
{: #data-transfer-cost}
{: faq}

將資料傳送至 {{site.data.keyword.cloud_notm}} 不會產生任何費用。


## 我可以使用 {{site.data.keyword.mdms_short}} 從 {{site.data.keyword.cloud_notm}} 匯出資料嗎？
{: #exporting-data}
{: faq}

目前，{{site.data.keyword.mdms_short}} 不支援從 {{site.data.keyword.cloud_notm}} 匯出資料。


## {{site.data.keyword.mdms_short}} 會加密我的資料嗎？
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}} 使用 AES 256 位元加密來加密所有資料，並提供一個高保護性密碼來解除鎖定儲存區。{{site.data.keyword.IBM}} 內的所有資料傳送都是透過 SSL 完成的。

## {{site.data.keyword.mdms_short}} 如何實際保護資料的安全？
{: #security}
{: faq}

所有 {{site.data.keyword.mdms_short}} 裝置都存放在堅固耐用的機殼中。這些外殼具有防水、防震及防竄改功能，可確保往返裝置及資料安全。

## 如何在整個移轉處理程序中追蹤我的要求？
{: #how-to-track-request}
{: faq}

若要追蹤要求的狀態，請導覽至 {{site.data.keyword.cloud_notm}} 主控台的 {{site.data.keyword.mdms_short}} 儀表板上的_要求詳細資料_ 標籤。

## 我的資料在卸載至 {{site.data.keyword.cos_full_notm}} 之後，您如何從 {{site.data.keyword.mdms_short}} 裝置中消除該資料？
{: #data-erasure}
{: faq}

在資料卸載至 IBM Cloud Object Storage 完成後，IBM 會立即使用 NIST 資料抹除標準來消除裝置，以確保完全消除裝置中的所有用戶端資料。

## {{site.data.keyword.mdms_short}} 的檔案介面為何？
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} 支援「網路檔案系統 (NFS)」和「伺服器訊息區塊 (SMB)」通訊協定。

## 如何使用 {{site.data.keyword.mdms_short}} 的檔案介面？
{: #how-to-use-file-interface}
{: faq}

首先，解除鎖定加密儲存區。然後，在包含要移轉的資料的伺服器上裝載共用。即會開始將資料檔案複製到網路共用。

## {{site.data.keyword.mdms_short}} 的檔案介面的好處為何？
{: #file-interface-benefits}
{: faq}

該檔案介面的基礎是成熟的檔案及網路軟體，可以將大量的大型檔案複製並傳輸到 {{site.data.keyword.cloud_notm}}。

## 如何將檔案儲存在 {{site.data.keyword.mdms_short}} 裝置上？
{: #file-storage}
{: faq}

{{site.data.keyword.mdms_short}} 裝置使用含有 LZ4 壓縮和 AES 256 位元加密的 ZFS 檔案系統。

## 在美國使用 {{site.data.keyword.mdms_short}} 需要多少成本？
{: #pricing-us}
{: faq}

在美國，每台裝置收取 395 美元的固定費用，包括 295 美元的裝置費用、100 美元的往返 UPS 隔日運送，以及現場使用 10 個營業日。

現場使用 10 天不包括將裝置運送給您的那天，也不包括您將裝置送回 IBM 的那天（最多兩天）。除了分配的 10 個營業日之外，如果還需要更多的時間才能完成移轉，則會針對額外使用的每一天，向您收取一天 30 美元的延期費用。

## 在歐盟使用 {{site.data.keyword.mdms_short}} 需要多少成本？
{: #pricing-eu}
{: faq}

在歐盟，每台裝置收取 445 美元的固定費用，包括 295 美元的裝置費用、150 美元的往返 FedEx 隔日運送，以及現場使用 10 個營業日。

現場使用 10 天不包括將裝置運送給您的那天，也不包括您將裝置送回 IBM 的那天（最多 2 天）。除了分配的 10 天之外，如果還需要更多的時間才能完成移轉，則會針對額外使用的每一天，向您收取一天 30 美元的延期費用。

## 在所有其他支援地區使用 {{site.data.keyword.mdms_short}} 需要多少成本？
{: #pricing-other}
{: faq}

在所有其他地區（日本、澳洲、巴西、加拿大、墨西哥、香港、新加坡、挪威及南韓），每台裝置收取 1,145 美元的固定費用，包括 295 美元的裝置費用、850 美元的往返運送，以及現場使用 10 個營業日。

現場使用 10 天不包括將裝置運送給您的那天，也不包括您將裝置送回 IBM 的那天（最多 2 天）。除了分配的 10 天之外，如果還需要更多的時間才能完成移轉，則會針對額外使用的每一天，向您收取一天 30 美元的延期費用。

這些地區提供特殊的運送需求。如需相關資訊，請參閱上述資訊。
{: note}

## 使用 {{site.data.keyword.cos_full_notm}} 需要付費嗎？
{: #pricing-cos}
{: faq}

將資料傳送到 {{site.data.keyword.cloud_notm}} 是免費的。不過，標準費率會套用於儲存在 {{site.data.keyword.cos_full_notm}} 或任何其他 {{site.data.keyword.cloud_notm}} 服務中的資料。若要進一步瞭解 Cloud Object Storage 中的計價選項，請參閱 [{{site.data.keyword.cos_full_notm}} 定價](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}。 

## 是否可以購買 {{site.data.keyword.mdms_full_notm}} 裝置？
{: #purchasing-devices}
{: faq}

無法購買 {{site.data.keyword.mdms_full_notm}} 裝置。

## {{site.data.keyword.mdms_short}} 處理程序如何保持物件名稱的唯一性？
{: #object-name-uniqueness}
{: faq}

為了確保物件複製到 Cloud Object Storage 儲存區時，其名稱是唯一的，會在物件名稱字首中併入檔案路徑。例如，`/root/user/config.ini` 在複製到儲存區時會變成 `root/user/config.ini`。

## 如果目標儲存區不存在於 {{site.data.keyword.cos_full_notm}} 帳戶，會發生什麼事？
{: #target-buckets}
{: faq}

如果目標儲存區不存在，則予以建立。如果它確實存在，則必須是空的，否則複製無法繼續進行。  

## 在掃描過程期間會跳過鏈結嗎？
{: #links-scan-process}
{: faq}

是的。在掃描過程期間，會跳過符號鏈結及固定鏈結。
