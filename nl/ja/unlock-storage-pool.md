---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# ストレージ・プールのロック解除
{: #unlock-storage-pool}

{{site.data.keyword.mdms_full}} デバイス用にプロビジョンされているストレージ・プールを最初にロック解除してアクティブ化することにより、デバイスにデータをコピーできます。
{: shortdesc}

## ストレージ・プール・パスフレーズの取得 (ベータ)
{: #retrieve-storage-pool-passcode}

{{site.data.keyword.mdms_short}} デバイスのストレージ・プールにアクセスするには、{{site.data.keyword.cloud_notm}} コンソールで {{site.data.keyword.mdms_short}} 要求の詳細にナビゲートして、デバイス資格情報を取得します。

このフィーチャーは、[{{site.data.keyword.mdms_short}} ベータ・リリース](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)の一部として使用可能です。 ストレージ・デバイスの資格情報には、[{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external} の_「要求の詳細」_セクションからアクセスすることもできます。
{: note}

ストレージ・プール・パスフレーズを取得するには、以下のようにします。

1. [{{site.data.keyword.cloud_notm}} コンソールにログインします](https://{DomainName}/){: external}。
2. **「メニュー」**&gt;**「リソース・リスト」**に移動し、リソースのリストを表示します。
3. {{site.data.keyword.cloud_notm}} リソース・リストで、{{site.data.keyword.mdms_short}} のプロビジョン済みインスタンスを選択します。
4. _「要求の詳細」_タブで、「資格情報」セクションにナビゲートします。
5. **「プール・ロック・パスコード (Pool lock passcode)」**の値をコピーします。

## ストレージ・プールのアクティブ化
{: #activate-storage-pool}

前のステップで取得した資格情報を使用して、空のストレージ・プールのロックを解除します。

1. [デバイス・ユーザー・インターフェースにログインします](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 「共通タスク」ウィザードで、**「ストレージ・プールのロックを解除して開始 (Unlock and Start Storage Pool)」**をクリックします。
3. ステップ 1 で取得したストレージ・プール・パスフレーズを入力し、**「OK」**をクリックします。
      
   ![ストレージ・プールのアクティブ化](/images/StartStoragePool.png)

   デフォルトで、共有には、アクセス制限なしで有効になっている、ネットワーク・ファイル・システム (NFS) プロトコルと Server Message Block (SMB) プロトコルの両方が含まれます。NFS または SMB のこの共有へのアクセス権限を変更するには、ユーザー・インターフェースで共有名を右クリックし、適切なメニュー・オプションを選択します。
   {: note}

## 次のステップ
{: #unlock-storage-pool-next-steps}

- Unix マシンを使用している場合は、[NFS を使用してネットワーク共有を接続します](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share)。
- Windows マシンを使用している場合は、[SMB を使用してネットワーク共有に接続します](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share)。
- [データ・コピー・プロセス](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy)を開始します。
