---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: copy data to device, move data to device, 

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

# デバイスへのデータのコピー
{: #copy-data}

デバイス・ユーザー・インターフェースを使用して、データを {{site.data.keyword.mdms_full}} デバイスにコピーできます。

## デバイスへのデータのコピー
{: #copy-data}

サーバーをネットワーク共有に接続した後、デバイスへのデータ・コピーを開始およびモニターできます。

1. ホスト・コンピューターと互換性のあるファイル・コピー・ツールを使用して、データをネットワーク共有にコピーします。
2. 「共通タスク」ウィザードで**「ネットワーク・アクティビティーの表示 (View Network Activity)」**をクリックすると、データが 10Gb リンクでデバイスに転送されているインバウンド・イーサネット・ロードが表示されます。
   
    ![アクティビティーの表示](images/NetworkPerf.png)
3. **「ストレージ・プールの表示 (View Storage pool)」**をクリックすると、デバイスのストレージの使用状況と IOPS をモニターできます。
   
    ![ストレージ・プールの表示](images/PoolPerf.png)

## 次のステップ
{: #import-data-next-steps}

- [デバイスの電源を正常に遮断します](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device)。
- 配送ラベルを用意して、[デバイスを {{site.data.keyword.cloud_notm}} に返送します](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device)。
