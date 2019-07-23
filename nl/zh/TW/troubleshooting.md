---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# 疑難排解
{: #troubleshooting}

{{site.data.keyword.mdms_full}} 的一般使用問題可能包括檢視訂單狀態或存取使用者介面。在許多情況下，您可以遵循一些簡單的步驟來解決這些問題。
{: shortdesc}

## 無法連接至 SMB 共用
{: #unable-to-mount-smb-share}

當您嘗試裝載 {{site.data.keyword.mdms_short}} 裝置上所佈建的「伺服器訊息區塊 (SMB)」共用時，無法連接至共用。 

您在加入 Active Directory 網域的 Windows 伺服器上使用 SMB 檔案傳送通訊協定。若要將資料移至 {{site.data.keyword.mdms_short}} 裝置，您需要連接至裝置上所佈建的網路共用。您可以對 IP 位址（其對應至裝置上的 10GbE 資料傳送埠）進行連線測試，但無法從伺服器裝載或連接至共用。
{: tsSymptoms}

將 {{site.data.keyword.mdms_short}} 裝置加入 Active Directory 之後，系統預設會啟用 SMB 簽署。SMB 簽署會消除攔截式攻擊的可能性，以在網路通訊期間增加額外的安全性。不過，SMB 簽署可能會影響資料傳送的網路效能，或導致[將共用裝載至伺服器時發生問題](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}。
{: tsCauses} 

如果您的環境未使用或不需要 SMB 簽署，則可以停用用戶端上的 SMB 簽署，以避免連線問題並增加資料傳送的效能。
{: tsResolve}

若要停用 Windows 伺服器上的 SMB 簽署，請將下列登錄機碼設為零：

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

若要進一步瞭解 SMB 簽署，請參閱[伺服器訊息區塊簽署概觀](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}。

## 無法檢視訂單詳細資料
{: #unable-to-view-order}

當您存取 {{site.data.keyword.cloud_notm}} 主控台時，無法檢視或追蹤您組織的 {{site.data.keyword.mdms_short}} 訂單。

您可以在 {{site.data.keyword.cloud_notm}} 資源清單中看到服務清單，但看不到 {{site.data.keyword.mdms_short}} 項目。
{: tsSymptoms}

您沒有檢視或追蹤 {{site.data.keyword.mdms_short}} 訂單的正確授權。
{: tsCauses} 

請向管理者確認，您已在適用的資源群組或服務實例中獲指派正確的角色。如需角色的相關資訊，請參閱[角色和許可權](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles)。
{: tsResolve}

## 取得協助及支援
{: #getting-help}

如果您在使用 {{site.data.keyword.mdms_short}} 裝置時有問題或疑問，可以搜尋「支援中心」中的資訊或直接聯繫我們來取得協助。

若要存取「支援中心」，請登入 {{site.data.keyword.cloud_notm}} 主控台，然後從功能表列中按一下**支援**。

您可以使用「支援中心」搜尋欄位，以在 {{site.data.keyword.cloud_notm}} 文件和 Stack Overflow 討論區中尋找問題的答案。您也可以從「支援中心」管理支援案例。在「支援中心」的「討論區」小節下，您可以針對技術問題尋找 Stack Overflow 討論區的鏈結，並針對所有其他問題尋找 IBM Developer Answers 討論區的鏈結。

如果您具有基本、進階或高階[支援方案](/docs/get-support?topic=get-support-support-plans#support-plans)，則可以尋找電話號碼和聊天選項來取得協助。

「支援中心」是取得支援的首選方法，但如果您無法登入 {{site.data.keyword.cloud_notm}}，則可以使用 [{{site.data.keyword.cloud_notm}} 服務入口網站](http://www.ibm.biz/bluemixsupport){: external}來提交案例。

如需開立 {{site.data.keyword.IBM_notm}} 支援問題單的相關資訊，或支援層次和問題單嚴重性的相關資訊，請參閱[與支援中心聯絡](/docs/get-support?topic=get-support-getting-customer-support){: external}。
