---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: user permissions, manage access, IAM roles

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

# 使用者存取權
{: #manage-access}

{{site.data.keyword.mdms_full}} 支援 {{site.data.keyword.iamlong}} 所控管的集中式存取控制系統，以協助您從 {{site.data.keyword.cloud_notm}} 主控台管理使用者以及對 {{site.data.keyword.mdms_short}} 要求的存取權。
{: shortdesc}

此功能是 {{site.data.keyword.mdms_short}} 測試版的一部分。若要進一步瞭解如何參與測試版計畫，請查看[取得測試版存取權](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)。
{: note}

## 角色和許可權
{: #roles}

身為帳戶擁有者，您可以在 {{site.data.keyword.cloud_notm}} 帳戶內設定原則，為不同的使用者建立不同層次的存取權。建立 {{site.data.keyword.mdms_short}} 要求之後，您將決定誰可以從 {{site.data.keyword.cloud_notm}} 主控台追蹤訂單的進度。

下表顯示 {{site.data.keyword.mdms_short}} 動作與 [{{site.data.keyword.cloud_notm}} IAM 平台管理角色](/docs/iam?topic=iam-userroles#iamusermanrol)的對映情況。 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>平台管理角色</th>
    <th>說明</th>
    <th>範例動作</th>
  </tr>
  <tr>
    <td><p>檢視者</p></td>
    <td><p>對於 {{site.data.keyword.cloud_notm}} 帳戶內的服務實例，檢視者具有僅限檢視存取權。檢視者無法建立或修改服務實例。</p></td>
    <td>
      <p>
        <ul>
          <li>存取 {{site.data.keyword.mdms_short}} 要求詳細資料頁面</li>
          <li>檢視 {{site.data.keyword.mdms_short}} 訂單的狀態</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>操作員</p></td>
    <td><p>操作員可以檢視服務實例、管理別名、連結及服務認證。</p></td>
    <td>
      <p>
        <ul>
          <li>不適用</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>編輯者</p></td>
    <td><p>編輯者具有操作員角色沒有的許可權，包括建立及刪除服務實例的能力。</p></td>
    <td>
      <p>
        <ul>
          <li>建立 {{site.data.keyword.mdms_short}} 要求。</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>管理者</p></td>
    <td><p>管理員可以執行檢視者、操作員及編輯者所能執行的所有動作，包括可邀請新使用者以及為其他使用者指派存取原則的能力。</p></td>
    <td>
      <p>
        <ul>
          <li>檢視者、操作員及編輯者可執行的所有動作</li>
          <li>指派使用者存取原則</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">表 1. 說明身分和存取角色與 {{site.data.keyword.mdms_short}} 許可權的對映情況</caption>
</table>

如需在使用者介面中指派使用者角色的相關資訊，請參閱[管理資源的存取權](/docs/iam?topic=iam-iammanidaccser#iammanidaccser)。
{: tip}



