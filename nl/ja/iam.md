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

# ユーザー・アクセス許可
{: #manage-access}

{{site.data.keyword.mdms_full}} では、ユーザーの管理および {{site.data.keyword.cloud_notm}} コンソールからの {{site.data.keyword.mdms_short}} 要求へのアクセスに役立つように、{{site.data.keyword.iamlong}} によって管理される集中アクセス制御システムをサポートしています。
{: shortdesc}

この機能は、{{site.data.keyword.mdms_short}} ベータ・リリースの一部として使用可能です。 ベータ・プログラムへの参加について詳しくは、[ベータ版へのアクセス](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)を参照してください。
{: note}

## 役割と許可
{: #roles}

アカウント所有者は、{{site.data.keyword.cloud_notm}} アカウント内にポリシーを設定して、さまざまなユーザー用にさまざまなレベルのアクセス権限を作成できます。 {{site.data.keyword.mdms_short}} 要求を作成した後に、{{site.data.keyword.cloud_notm}} コンソールから注文の進行を追跡できるユーザーを決定します。

以下の表は、{{site.data.keyword.mdms_short}} アクションが [{{site.data.keyword.cloud_notm}} IAM プラットフォーム管理役割](/docs/iam?topic=iam-userroles#iamusermanrol)にどのようにマップされるかを示しています。 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>プラットフォーム管理役割</th>
    <th>説明</th>
    <th>アクションの例</th>
  </tr>
  <tr>
    <td><p>Viewer</p></td>
    <td><p>ビューアーには、{{site.data.keyword.cloud_notm}} アカウント内のサービス・インスタンスに対する表示専用アクセス権限があります。 ビューアーは、サービス・インスタンスを作成したり、変更したりできません。</p></td>
    <td>
      <p>
        <ul>
          <li>{{site.data.keyword.mdms_short}} 要求の詳細ページへのアクセス</li>
          <li>{{site.data.keyword.mdms_short}} 注文の状況の表示</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Operator</p></td>
    <td><p>オペレーターは、サービス・インスタンスの表示、別名、バインディング、およびサービス資格情報の管理を行うことができます。</p></td>
    <td>
      <p>
        <ul>
          <li>適用外</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Editor</p></td>
    <td><p>エディターには、サービス・インスタンスの作成と削除など、オペレーター役割を超えた権限があります。</p></td>
    <td>
      <p>
        <ul>
          <li>{{site.data.keyword.mdms_short}} 要求を作成します。</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>管理者</p></td>
    <td><p>管理者は、新規ユーザーの招待、および他のユーザーに対するアクセス・ポリシーの割り当てなど、ビューアー、オペレーター、およびエディターが実行できるすべてのアクションを実行できます。</p></td>
    <td>
      <p>
        <ul>
          <li>ビューアー、オペレーター、およびエディターが実行できるすべてのアクション</li>
          <li>ユーザー・アクセス・ポリシーの割り当て</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">表 1. ID およびアクセス役割が {{site.data.keyword.mdms_short}} 許可にどのようにマップされるのかについての説明</caption>
</table>

UI でのユーザーの役割の割り当てについては、[リソースに対するアクセス権限の管理](/docs/iam?topic=iam-iammanidaccser#iammanidaccser)を参照してください。
{: tip}



