---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount SMB share, SMB, Active Directory, AD, access network share, connect to network share

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

# 使用 SMB 連接至網路共用
{: #connect-smb-share}

若要準備資料複製，您可以使用「伺服器訊息區塊 (SMB)」通訊協定，在 {{site.data.keyword.mdms_full}} 裝置上存取網路共用。
{: shortdesc}

連接至共用之前，請執行下列動作：

- 判定是否需要將 {{site.data.keyword.mdms_short}} 裝置加入 Active Directory。如果您要將網路共用裝載至已加入 Active Directory 的 Windows 伺服器，則還必須先[將裝置加入 Active Directory 網域](#use-active-directory)，才能連接至共用。
- 判定您的環境是否需要 SMB 簽署。將 {{site.data.keyword.mdms_short}} 裝置加入 Active Directory，依預設會啟用 SMB 簽署。如果您的環境不需要 SMB 簽署，則可以[停用用戶端上的 SMB 簽署](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share)，以避免連線問題並增加資料傳送的效能。

## 管理 SMB 共用存取權
{: #manage-smb-share-access}

依預設，網路共用會設為具有公用存取權。在將共用裝載至伺服器之前，您可以在共用上新增 SMB 存取規則，以符合您的環境或安全需求。 

如需控制儲存裝置上共用存取權的詳細資訊，請參閱 [OSNEXUS QuantaStor 文件](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}。
{: tip}

若要修改 SMB 共用存取權，請執行下列動作：

1. [登入裝置使用者介面](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 在「一般作業」精靈中，按一下**檢視網路共用**，以顯示網路共用視圖。

   ![工作流程圖示](images/workflow.png)

3. 關閉「一般作業」精靈，然後在網路共用名稱上按一下滑鼠右鍵來檢視選項清單。 
4. 按一下**修改共用和 SMB 存取**，來修改 SMB 共用的存取權。

    ![修改 SMB 共用的存取權](images/add-smb-access.png)

## 使用 Active Directory
{: #use-active-directory}

如果您要在 Windows 伺服器上使用 SMB，可以藉由將 {{site.data.keyword.mdms_short}} 裝置加入 Active Directory，來管理資料的存取權、檔案所有權及檔案屬性。將裝置加入 Active Directory 網域，可讓 SMB 存取特定的 AD 使用者和 AD 群組。 

若要進一步瞭解如何將裝置加入 Active Directory，請參閱 [OSNEXUS QuantaStor 文件](https://wiki.osnexus.com/index.php?title=Network_Shares#Joining_an_AD_Domain){:external}。

## 在 Windows 系統上裝載 SMB 共用
{: #mount-smb-share}

在您解除鎖定並啟動裝置上的儲存區之後，請使用 Windows 電腦上的**對映網路磁碟機**對話框來連接至 SMB 共用。

若要裝載網路共用，請執行下列動作：

1. [登入裝置使用者介面](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 在「一般作業」精靈中，按一下**檢視網路共用**，以顯示網路共用視圖。
3. 關閉「一般作業」精靈，然後在網路共用名稱上按一下滑鼠右鍵來檢視選項清單。 
4. 按一下**檢視裝載指令**，來檢閱共用的裝載資訊。
5. 對對話框中列出的 IP 位址進行連線測試，以測試電腦與 {{site.data.keyword.mdms_short}} 裝置之間的網路連線功能。

   請確定 IP 位址對應至裝置上的 [10GbE 資料傳送埠](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings)。
   {: note} 
6. 從「檔案總管」中，在**網路**上按一下滑鼠右鍵，然後選取**對映網路磁碟機**來開啟「對映網路磁碟機」對話框。

   ![開啟對映網路磁碟機對話框](images/map-network-drive.png)
7. 輸入您在步驟 1 中測試的 IP 位址，然後按一下**瀏覽**。

   ![連接至網路共用](images/map-network-drive-dialog.png)
8. 從網路資料夾清單中，選取 {{site.data.keyword.mdms_short}} 共用。按一下**確定**，以確認。
9. 按一下**完成**，在來源伺服器上裝載共用。

    如果您能夠對 IP 位址進行連線測試，但無法裝載共用，則可能是已針對 Windows 用戶端啟用 SMB 簽署。請考量在用戶端上[停用 SMB 簽署](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share)，然後再試一次。
    {: tip} 

## 後續步驟
{: #connect-smb-share-next-steps}

- 啟動[資料複製處理程序](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data)。
