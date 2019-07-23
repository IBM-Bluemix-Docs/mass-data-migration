---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# {{site.data.keyword.mdms_short}} の概要
{: #about}

{{site.data.keyword.mdms_full}} は、テラバイト単位からペタバイト単位までのデータを {{site.data.keyword.cloud_notm}} に物理的に転送するための高速かつシンプルでセキュアな方法を提供します。
{: shortdesc}

## {{site.data.keyword.mdms_short}} を選ぶ理由
{: #use-cases}

{{site.data.keyword.mdms_short}} は、データのマイグレーションを容易にする、ポータブルで事前構成されたストレージ・デバイスを提供することによって、クラウドに移行するプロセスの単純化に役立ちます。{{site.data.keyword.mdms_short}} のフィーチャーおよびユース・ケースについて詳しくは、以下のビデオを参照してください。

<iframe class="embed-responsive-item" id="youtubeplayer" title="IBM Cloud にデータを高速、シンプルかつセキュアに転送する方法を提供する Mass Data Migration" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


| ユース・ケース| 説明 |
| --- | --- |
| クラウドへのデータ・マイグレーション | オンプレミスのストレージ・スペースの解放、非アクティブ・データのアーカイブ、または冗長化と復旧のためのデータのバックアップのいずれを希望する場合でも、{{site.data.keyword.mdms_short}} なら、データをクラウドに素早くセキュアに移動できます。 |
| データ・センターの閉鎖 | データ・センターの転換をすぐに始めて、{{site.data.keyword.mdms_short}} を使用することで、データ・センターの縮小、拡張、再配置にあわせて重要データをクラウドにセキュアに移動できます。 |
| 帯域幅の制限 | リモート・ロケーションにいる場合や、ネットワーク経由オプションが桁違いの費用がかかる、遅すぎる、またはデータ転送に使用できないなどの問題が発覚した場合は、{{site.data.keyword.mdms_short}} が優れた代替手段となります。 |
{: caption="表 1. {{site.data.keyword.mdms_short}} のユース・ケースの説明 " caption-side="top"}

[データ・マイグレーション・ソリューションを探索](https://www.ibm.com/cloud/data-migration)すると、{{site.data.keyword.cloud_notm}} のデータ・マイグレーション・オプションを比較できます。{{site.data.keyword.mdms_short}} のフィーチャーと利点について詳しくは、[{{site.data.keyword.mdms_short}} の製品ページ](https://www.ibm.com/cloud/mass-data-migration){: external}を参照してください。
{: tip}

## 仕組み
{: #how-it-works}

{{site.data.keyword.mdms_short}} では、120 TB の使用可能容量のあるストレージ・デバイスを使用して、クラウドへのデータ移動を加速します。データ転送に関わる一般的な問題点 (高コスト、長い転送時間、セキュリティーの問題など) を解決できます。

以下の図は、{{site.data.keyword.mdms_short}} のプロセスを説明しています。

![Mass Data Migration のプロセスを説明します。](images/mdms-workflow.png)

## サービス・コンポーネント
{: #service-componenets}

{{site.data.keyword.mdms_short}} は、以下のサービス・コンポーネントで構成されています。

<dl>
   <dt>{{site.data.keyword.mdms_short}} ダッシュボード</dt>
      <dd><a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a> のサービス・ダッシュボードで {{site.data.keyword.mdms_short}} の注文を作成および追跡できます。 {{site.data.keyword.mdms_short}} 要求ページで、ネットワーク構成の設定を指定し、デバイスにログインするための資格情報を取得して、注文の状況を追跡します。 </dd>
   <dt>{{site.data.keyword.mdms_short}} デバイス</dt>
      <dd>{{site.data.keyword.mdms_short}} は、配送場所に輸送される<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">ポータブル・ストレージ・デバイス</a>を提供します。 {{site.data.keyword.mdms_short}} デバイスは、事前構成され、ネットワークに接続する準備が整った状態で届きます。</dd>
   <dt>デバイス・ユーザー・インターフェース</dt>
      <dd><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">デバイス・ユーザー・インターフェース</a>は、{{site.data.keyword.mdms_short}} デバイス上のネットワーク共有にアクセスするために使用する Web ベースのローカル UI です。 この UI は安定したファイル/ネットワーク・ソフトウェアに基づいているので、多数の巨大なファイルをコピーして {{site.data.keyword.cloud_notm}} に転送できます。</dd>
</dl>










