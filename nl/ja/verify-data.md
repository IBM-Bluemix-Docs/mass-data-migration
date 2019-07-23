---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# データの検証
{: #verify-data}

{{site.data.keyword.cos_full}} を使用して、マイグレーション済みデータにアクセスし、検証できます。
{: shortdesc}

オフロードが完了した後、デバイスのデータが {{site.data.keyword.cloud_notm}} によって安全に消去されている間にも、クラウド上のデータにすぐにアクセスできます。

## Cloud Object Storage 内のデータへのアクセス
{: #access-data-cos}

マイグレーションされたデータは、{{site.data.keyword.mdms_short}} 要求を送信するときに指定した Cloud Object Storage インスタンスで使用可能です。ソース・サーバーからデータを削除する前に、データが {{site.data.keyword.cloud_notm}} に正常にアップロードされたことを確認します。

データにアクセスして検証するには、以下のようにします。 

1. [{{site.data.keyword.cloud_notm}} コンソールにログインします](https://{DomainName}/){: external}。
2. **「メニュー」**&gt;**「リソース・リスト」**に移動し、リソースのリストを表示します。
3. {{site.data.keyword.cloud_notm}} リソース・リストで、Cloud Object Storage のプロビジョン済みインスタンスを選択します。
4. 使用可能なストレージ・バケットのリストから、データ・マイグレーション用に指定したバケット名を選択します。
5. バケットに関連付けられているオブジェクトが、{{site.data.keyword.mdms_short}} デバイスにコピーしたデータに対応していることを確認します。

## 別のストレージ・ソリューションへのデータの移動
{: #move-data}

ワークロード要件に応じて、マイグレーションしたデータを Cloud Object Storage から別のクラウド・ストレージ・ソリューション ([ファイル・ストレージ](https://{DomainName}/catalog/infrastructure/file-storage)や[ブロック・ストレージ](https://{DomainName}/catalog/infrastructure/block-storage)など) に移動しなければならない場合があります。 

ストレージ・マイグレーションのオプションについて詳しくは、[レシピ: Moving data from COS to File or Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external} を参照してください。

