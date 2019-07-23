---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# 入門指導教學
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} 可協助您以快速、簡單且安全的方式，將數 TB 到數 PB 的資料移至 {{site.data.keyword.cloud_notm}}。本指導教學示範如何使用 {{site.data.keyword.slportal}} 來要求移轉裝置。
{: shortdesc}

有興趣嘗試新的 {{site.data.keyword.mdms_short}} 特性嗎？您可以參與 {{site.data.keyword.mdms_short}} 測試版計畫，來預覽即將提供的服務加強功能。若要瞭解更多相關資訊，請參閱[取得測試版的存取權](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)。
{: tip}

## 開始之前
{: #get-started-prereqs}

訂購 {{site.data.keyword.mdms_short}} 裝置之前，請執行下列動作：

- 檢閱有提供 {{site.data.keyword.mdms_short}} 的[地區和位置](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions)，以規劃移轉。
- 確定您具有已為 {{site.data.keyword.cloud_notm}} 帳戶佈建的 [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} 實例。 
- 瞭解網路連線類型和速度。
- 收集 IP 位址及其他遞送詳細資料這類網路設定，以將裝置連接至來源伺服器。
- 識別可在您的網站接收、連接及使用裝置的人員。

## 建立儲存空間儲存區
{: #get-started-create-bucket}

佈建 Cloud Object Storage 的實例之後，請建立儲存空間儲存區來設定已移轉資料的目的地。 

1. 從 {{site.data.keyword.cloud_notm}} 資源清單中，選取您已佈建的 Cloud Object Storage 實例。
2. 從_開始使用_ 頁面中，按一下**建立儲存區**。
3. 輸入儲存區名稱，然後為您的資料選取一個備援選項。
   
   備援選項決定將資料匯入至 Cloud Object Storage 服務之後，該服務如何在一個地理區域中分散您的資料。{{site.data.keyword.mdms_short}} 支援可用於 Cloud Object Storage 的所有備援選項。  
   {: note}
4. 從位置清單中，選取將資料移轉至儲存空間儲存區之後要實際儲存資料的地理區域。
5. 從儲存空間類別清單中，選取**標準**。
6. 按一下**建立儲存區**。

## 要求裝置
{: #get-started-request-device}

您可以使用 {{site.data.keyword.slportal}} 來要求 {{site.data.keyword.mdms_short}} 裝置。

1. 登入 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}。
2. 從導覽功能表中，按一下**儲存空間** > **資料移轉** > **{{site.data.keyword.mdms_short}}**，以存取 {{site.data.keyword.mdms_short}} 登入頁面。
3. 按一下**要求裝置**，以開啟訂單表格。
4. 指定下列詳細資料，以啟動 {{site.data.keyword.mdms_short}} 要求。

    <table>
      <tr>
        <th>動作</th>
        <th>說明</th>
      </tr>
      <tr>
        <td>新增要求名稱</td>
        <td>輸入別名，以識別並追蹤 {{site.data.keyword.mdms_short}} 要求。</td>
      </tr>
      <tr>
        <td>選取資料卸載目的地</td>
        <td>從下拉清單中，選取您已佈建的 Cloud Object Storage 實例。然後，選取您指派給儲存空間儲存區的名稱，您要在該儲存空間儲存區中儲存已移轉資料。</td>
      </tr>
      <tr>
        <td>新增運送地址</td>
        <td>輸入運送資訊，例如運送地址以及將接受交付的人員名稱。</td>
      </tr>
      <tr>
        <td>新增移轉聯絡人</td>
        <td>輸入將管理裝置資料移轉的人員名稱。</td>
      </tr>
      <tr>
        <td>配置網路設定</td>
        <td>
          <p>輸入網路配置詳細資料，來配置資料傳送連線的設定。</p>
          <p>提供下列<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">網路設定</a>：</p>
          <p>
            <ul>
              <li><i>裝置管理設定。</i>輸入遠端電腦的靜態 IP 位址、網路遮罩及預設閘道。</li>
              <li><i>資料傳送設定。</i>輸入來源資料所在伺服器的靜態 IP 位址及網路遮罩。</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">表 1. 說明 {{site.data.keyword.mdms_short}} 要求工作流程</caption>
    </table>

    當您選取裝置的交付位置時，請考量裝置的重量及可存取性。裝置、其硬殼和泡棉運輸箱的重量約 60 磅。為了協助運輸裝置，運輸箱配備可輕鬆操作的輪子和彈出式把手。
    {: tip}
5. 閱讀 {{site.data.keyword.mdms_short}} 服務合約，然後選取勾選框。
6. 按一下**工作區要求**，以完成訂單。 

## 下一步為何？
{: #get-started-next-steps}

成功！您已設定好 {{site.data.keyword.mdms_short}} 要求。

- 若要進一步瞭解如何追蹤訂單，請查看[管理要求](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)。
- 若要進一步瞭解如何接收及連接裝置，請查看[設定裝置](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview)。

