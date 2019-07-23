---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: migrate Netezza databases, PureData System for Analytics databases, 

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

# PureData System for Analytics データベースの {{site.data.keyword.dashdbshort_notm}} へのマイグレーション
{: #migrate-netezza-databases}

{{site.data.keyword.mdms_full}} を使用して、大規模な IBM PureData™ System for Analytics (Netezza® テクノロジーを採用) データベースを {{site.data.keyword.dashdbshort}} にマイグレーションできます。 本資料は、転送するデータの量と、エクスポート方法を決定するツールのリファレンスとして使用できます。
{: shortdesc}

## データベース・オブジェクトのサイズの決定
{: #determine-db-object-size}

1. [IBM Support > Fix Central > Netezza Tools ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window} から、ご使用の Netezza インスタンスに対応するバージョンの Netezza ツールをダウンロードしてください。

   デフォルトでは、サポート・ツールは、Netezza サーバーの `/nz/support-IBM_Netezza<version>/bin` ディレクトリーにインストールされます
   {:note}

2. 以下の 2 つのコマンドを実行します。
   - `nz_db_size`: データベースのサイズを決定します

     ```
     nz_db_size
     Object | Name | Bytes | KB | MB | GB | TB
     -----------------------------------------------------------------------------------------------------------
     Appliance | cdcntze1 | 23,388,712,337,408 | 22,840,539,392 | 22,305,214 | 21,782.4 | 21.3
     Database | DHDB | 183,537,500,160 | 179,235,840 | 175,035 | 170.9 | .2
     Table | DH71964I1 | 880,803,840 | 860,160 | 840 | .8 | .0
     Table | DH71964T1 | 96,120,078,336 | 93,867,264 | 91,667 | 89.5 | .1
     Table | DH71964T10 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T2 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T3 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T4 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T5 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T6 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T7 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T8 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T9 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     ```
     {: codeblock}

   - `nz_compressedTableRatio`: 圧縮解除後のデータのサイズを見積もります。

      ```
      nz_compressedTableRatio
  ....................................................................................
      . The values below show the estimated size ratio of a compressed table to its .
      . uncompressed form. An uncompressed table is approximately <ratio> times larger .
      . than its compressed version. .
      . .
      . The 'Compressed Size' is the actual amount of storage being used by the table. .
      . The 'Uncompressed Size' is an estimate based on mathematical calculations. .
      ....................................................................................
      Database: DHDB
      Table/MView Name Ratio Compressed Size Uncompressed Size Size Difference
      ================== ===== ================ =============== ===========
      DH71964I1 1.49 880,803,840 1,310,723,840 429,920,000
      DH71964T1 1.50 96,120,078,336 144,179,203,840 48,059,125,504
      DH71964T10 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T2 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T3 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T4 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T5 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T6 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T7 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T8 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T9 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      ================================ ===== =================== ===================
      Total For This Database 1.50 183,537,500,160 275,251,242,240 91,713,742,080
      ```
      {: codeblock}

## データの抽出とオンボード
{: #extract-data}

Netezza からデータを抽出する方法として、2 つのオプションがあります。
- `nz_backup` ユーティリティーを使用する。
   ```
   /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
   ```

   `{target_directory}` は、このサーバーにマウントした、MDMS デバイスの NFS 共有です。
   {:tip}

- `CREATE EXTERNAL TABLE` ステートメントを使用する。
   - `FORMAT` として ”Text”を選択してください
   - `LOAD` プロセスでエクスポート/再利用のために使用した `USING` 節を {{site.data.keyword.dashdbshort_notm}} チームに伝えてください。


## データの検証
{: #validate-data}

外部表 `myfile` と `USING(....)` 節を指定して `SELECT FROM` ステートメントを使用することによって Netezza にデータを再び読み込み、データが正しいかどうかを確認できます。

**追加情報**

PureData System for Analytics について詳しくは、[IBM Netezza データベース・ユーザー資料 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}を参照してください。
