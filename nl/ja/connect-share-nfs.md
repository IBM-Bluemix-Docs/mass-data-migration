---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount NFS share, NFS, access network share, connect to network share

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

# NFS を使用したネットワーク共有への接続
{: #connect-nfs-share}

データ・コピーの準備をするには、ネットワーク・ファイル・システム (NFS) プロトコルを使用して {{site.data.keyword.mdms_full}} デバイス上のネットワーク共有にアクセスします。
{: shortdesc}

共有に接続する前に、以下のことを行います。

- クライアントに `nfs-common` などの NFS ソフトウェアがインストールされていることを確認します。 `nfs-common` パッケージをインストールするには、端末セッションから `sudo apt install nfs-common` を実行します。

## NFS 共有へのアクセスの管理
{: #manage-nfs-share-access}

デフォルトでは、ネットワーク共有は公開アクセスを持つように設定されています。 共有をサーバーにマウントする前に、ご使用の環境またはセキュリティー要件に合わせて、共有に NFS アクセス規則を追加できます。 

ストレージ・デバイスの共有へのアクセスの制御について詳しくは、[OSNEXUS QuantaStor の資料](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}を参照してください。
{: tip}

NFS 共有のアクセス権限を変更するには、以下のようにします。

1. [デバイス・ユーザー・インターフェースにログインします](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 「共通タスク」ウィザードで**「ネットワーク共有の表示 (View Network Shares)」**をクリックすると、ネットワーク共有のビューが表示されます。

   ![ワークフロー・アイコン](images/workflow.png)
3. 「共通タスク」ウィザードを閉じてから、ネットワーク共有名を右クリックすると、オプションのリストが表示されます。 
4. **「NFS アクセスの追加 (Add NFS Access)」**をクリックして、NFS 共有のアクセス権限を変更します。

    ![NFS 共有のアクセス権限の変更](images/add-nfs-access.png)

## UNIX システムでの NFS 共有のマウント
{: #mount-nfs-share}

デバイスのストレージ・プールをアンロックしてアクティブ化した後に、{{site.data.keyword.mdms_short}} デバイス・ユーザー・インターフェースを使用して UNIX ベースのシステム上の NFS 共有に接続できます。

ネットワーク共有をマウントするには、以下のようにします。 

1. [デバイス・ユーザー・インターフェースにログインします](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui)。
2. 「共通タスク」ウィザードで**「ネットワーク共有の表示 (View Network Shares)」**をクリックすると、ネットワーク共有のビューが表示されます。
3. 「共通タスク」ウィザードを閉じてから、ネットワーク共有名を右クリックすると、オプションのリストが表示されます。 
4. **「マウント・コマンドの表示 (View Mount Command)」**をクリックして、共有のマウント情報を確認します。

    以下の図は、値の例を含む「マウント・コマンドの表示 (View Mount Command)」ダイアログ・ボックスを示しています。

    ![共有のマウント](images/mount-command.png)

    _「ネットワーク・ポート」_の値は、{{site.data.keyword.mdms_short}} デバイスのデータ転送ポートに対応します。_「マウント・コマンド (Mount command)」_の値は、共有のマウントおよび接続に使用されるコマンドを指定します。
5. ダイアログ・ボックスにリストされている IP アドレスに ping して、ご使用のコンピューターと {{site.data.keyword.mdms_short}} デバイスの間のネットワーク接続をテストします。

   IP アドレスがデバイスの [10GbE データ転送ポート](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings)に対応していることを確認します。
   {: note}  
6. ダイアログ・ボックスにリストされているマウント・コマンドをコピーして、ご使用のコンピューターの端末セッションに貼り付けます。
7. このコマンドを実行すると、共有がサーバーにマウントされます。

## 次のステップ
{: #connect-nfs-share-next-steps}

- [データ・コピー・プロセス](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data)を開始します。
