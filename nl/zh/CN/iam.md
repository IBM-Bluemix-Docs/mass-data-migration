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

# 用户访问许可权
{: #manage-access}

{{site.data.keyword.mdms_full}} 支持由 {{site.data.keyword.iamlong}} 管理的集中式访问控制系统，以帮助您通过 {{site.data.keyword.cloud_notm}} 控制台来管理用户和访问 {{site.data.keyword.mdms_short}} 请求。
{: shortdesc}

此功能在 {{site.data.keyword.mdms_short}} Beta 发行版中提供。要了解有关参与 Beta 程序的更多信息，请查看[获取 Beta 访问权](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)。
{: note}

## 角色和许可权
{: #roles}

作为帐户所有者，您可以在 {{site.data.keyword.cloud_notm}} 帐户中设置策略，以针对不同用户创建不同级别的访问权。创建 {{site.data.keyword.mdms_short}} 请求后，您可决定谁可以通过 {{site.data.keyword.cloud_notm}} 控制台来跟踪订单的进度。

下表显示了 {{site.data.keyword.mdms_short}} 操作与 [{{site.data.keyword.cloud_notm}} IAM 平台管理角色](/docs/iam?topic=iam-userroles#iamusermanrol)的映射关系。 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>平台管理角色</th>
    <th>描述</th>
    <th>示例操作</th>
  </tr>
  <tr>
    <td><p>查看者</p></td>
    <td><p>查看者具有对 {{site.data.keyword.cloud_notm}} 帐户中服务实例的仅查看访问权。查看者无法创建或修改服务实例。</p></td>
    <td>
      <p>
        <ul>
          <li>访问 {{site.data.keyword.mdms_short}} 请求详细信息页面</li>
          <li>查看 {{site.data.keyword.mdms_short}} 订单的状态</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>操作员</p></td>
    <td><p>操作员可以查看服务实例，管理别名、绑定和服务凭证。</p></td>
    <td>
      <p>
        <ul>
          <li>不适用</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>编辑者</p></td>
    <td><p>编辑者的许可权范围超过操作员角色，包括创建和删除服务实例的能力。</p></td>
    <td>
      <p>
        <ul>
          <li>创建 {{site.data.keyword.mdms_short}} 请求。</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>管理员</p></td>
    <td><p>管理者可以执行查看者、操作员和编辑者能够执行的所有操作，包括邀请新用户和为其他用户分配访问策略的能力。</p></td>
    <td>
      <p>
        <ul>
          <li>查看者、操作员和编辑者可以执行的所有操作</li>
          <li>分配用户访问策略</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">表 1. 描述身份和访问角色与 {{site.data.keyword.mdms_short}} 许可权的映射关系</caption>
</table>

有关在 UI 中分配用户角色的信息，请参阅[管理对资源的访问权](/docs/iam?topic=iam-iammanidaccser#iammanidaccser)。
{: tip}



