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

# トラブルシューティング
{: #troubleshooting}

{{site.data.keyword.mdms_full}} の使用に関する一般的な問題には、注文状況の表示やユーザー・インターフェースへのアクセスなどがあります。多くの場合、いくつかの簡単なステップを実行することで、これらの問題から復旧することが可能です。
{: shortdesc}

## SMB 共有に接続できない
{: #unable-to-mount-smb-share}

{{site.data.keyword.mdms_short}} デバイスでプロビジョンされた Server Message Block (SMB) 共有のマウントを試行しても、共有に接続できません。 

Active Directory ドメインに結合された Windows サーバーで SMB ファイル転送プロトコルを使用しています。{{site.data.keyword.mdms_short}} デバイスにデータを移動するには、デバイスでプロビジョンされたネットワーク共有に接続する必要があります。デバイスで 10GbE データ転送ポートに対応する IP アドレスを ping することはできますが、サーバーから共有をマウントしたり接続したりすることはできません。
{: tsSymptoms}

{{site.data.keyword.mdms_short}} デバイスを Active Directory に結合すると、システムはデフォルトで SMB 署名を有効にします。SMB 署名は、中間者攻撃の可能性を排除することにより、ネットワーク通信中のセキュリティーを向上させます。ただし、SMB 署名は、データ転送のネットワーク・パフォーマンスに影響を与えたり、[サーバーに共有をマウントする場合の問題](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external} の原因になったりする可能性があります。
{: tsCauses} 

ご使用の環境で SMB 署名を使用しない場合、または必要としない場合は、クライアントで SMB 署名を無効にすると、接続の問題を回避してデータ転送のパフォーマンスを向上させることができます。
{: tsResolve}

Windows サーバーで SMB 署名を無効にするには、以下のレジストリー・キーをゼロに設定します。

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

SMB 署名について詳しくは、[Overview of Server Message Block signing](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external} を参照してください。

## 注文の詳細を表示できない
{: #unable-to-view-order}

{{site.data.keyword.cloud_notm}} コンソールにアクセスしたときに、組織の {{site.data.keyword.mdms_short}} 注文を表示したり追跡したりできません。

{{site.data.keyword.cloud_notm}} リソース・リストにサービスのリストは表示されますが、{{site.data.keyword.mdms_short}} 項目が表示されません。
{: tsSymptoms}

{{site.data.keyword.mdms_short}} 注文を表示または追跡するための適切な許可がありません。
{: tsCauses} 

該当するリソース・グループまたはサービス・インスタンスにおいて正しい役割を割り当てられているかどうか、管理者と共に検証してください。 役割について詳しくは、[役割と許可](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles)を参照してください。
{: tsResolve}

## ヘルプおよびサポートの利用
{: #getting-help}

{{site.data.keyword.mdms_short}} デバイスの使用中に問題や質問が生じた場合は、サポート・センターで情報を検索するか、直接お問い合わせください。

サポート・センターにアクセスするには、{{site.data.keyword.cloud_notm}} コンソールにログインし、メニュー・バーで**「サポート」**をクリックします。

サポート・センターの検索フィールドを使用して、{{site.data.keyword.cloud_notm}} 資料およびスタック・オーバーフロー・フォーラム全体から疑問点に対する回答を見つけることができます。サポート・センターからサポート Case を管理することもできます。 サポート・センターの「フォーラム」セクションに、技術的質問向けのスタック・オーバーフロー・フォーラムへのリンクと、その他のすべての質問向けの IBM Developer Answers フォーラムへのリンクの両方があります。

[サポート・プラン](/docs/get-support?topic=get-support-support-plans#support-plans)が基本、アドバンスト、またはプレミアムの場合、ヘルプを利用するための電話番号およびチャット・オプションが提供されます。

サポート・センターの利用は、サポートを受ける上で望ましい方法ですが、{{site.data.keyword.cloud_notm}} にログインできない場合は、[{{site.data.keyword.cloud_notm}} サービス・ポータル](http://www.ibm.biz/bluemixsupport){: external} を使用して Case を送信できます。

{{site.data.keyword.IBM_notm}} サポート・チケットのオープン、またはサポート・レベルおよびチケットの重大度について詳しくは、[サポートへのお問い合わせ](/docs/get-support?topic=get-support-getting-customer-support){: external} を参照してください。
