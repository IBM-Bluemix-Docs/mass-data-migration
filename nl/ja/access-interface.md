---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# デバイス・ユーザー・インターフェースへのアクセス
{: #access-ui}

{{site.data.keyword.mdms_full}} デバイスをイーサネット接続用に構成すると、デバイス・ユーザー・インターフェースにアクセスできるようになるため、デバイスと対話してデータ・マイグレーション・プロセスを開始できます。
{: shortdesc}

## デバイス資格情報の取得 (ベータ)
{: #retrieve-device-credentials}

{{site.data.keyword.mdms_short}} 要求を送信すると、サービスによって、デバイスのローカル Web UI にアクセスするために使用できる資格情報が自動生成されます。 

このフィーチャーは、[{{site.data.keyword.mdms_short}} ベータ・リリース](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)の一部として使用可能です。 ストレージ・デバイスの資格情報には、[{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} の_「要求の詳細」_セクションからアクセスすることもできます。
{: note}

デバイスの資格情報を取得するには、以下のようにします。

1. [{{site.data.keyword.cloud_notm}} コンソールにログインします](https://{DomainName}/){: external}。
2. **「メニュー」**&gt;**「リソース・リスト」**に移動し、リソースのリストを表示します。
3. {{site.data.keyword.cloud_notm}} リソース・リストで、{{site.data.keyword.mdms_short}} のプロビジョン済みインスタンスを選択します。
4. _「要求の詳細」_タブで、「資格情報」セクションにナビゲートします。
5. **「ユーザー名」**および**「パスワード」**の値をコピーします。

## デバイス・ユーザー・インターフェースへのログイン
{: #log-in-ui}

前の手順で取得したデバイスの資格情報を使用して、ローカル Web UI にログインし、{{site.data.keyword.mdms_short}} デバイスと対話します。

1. Web ブラウザーを開いて、注文フォームに指定した静的 IP アドレスにナビゲートします。

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   `<device_management_IP_address>` を、Eth1 または Eth2 ネットワーク・ポート用に構成された IP アドレスで置き換えます。 証明書の例外は、そのまま受け入れます。

2. 前の手順で取得したユーザー名とパスワードを使用して、デバイス UI にログインします。 

   ![ログイン・ページ](images/login.png)
   
   「共通タスク」ウィザードが表示されます。 左から右のオプションを使用して、データのインポートを開始します。

   ![ワークフロー・アイコン](images/workflow.png)

   「共通タスク」ウィザードを再度開くには、インターフェースの左上領域にある**「ワークフロー・マネージャー」**を使用します。
   {:tip}

## 次のステップ
{: #access-ui-next-steps}

- データ取り込みコピーを準備するには、まず、[デバイス上のストレージ・プールをアンロック](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool)します。
