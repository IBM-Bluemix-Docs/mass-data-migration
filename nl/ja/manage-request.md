---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

# 要求の管理
{: #manage-request}

{{site.data.keyword.slportal}} を使用して、{{site.data.keyword.mdms_full}} の注文の状況を管理および追跡します。
{: shortdesc}

{{site.data.keyword.mdms_short}} ベータ・プログラムに参加すると、{{site.data.keyword.cloud_notm}} コンソールからアクセスできる新しい {{site.data.keyword.mdms_short}} サービス・ダッシュボードをプレビューできます。 詳しくは、[ベータ版へのアクセス](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)を参照してください。
{: tip}

## 注文の追跡 
{: #track-order}

ストレージ・デバイスを要求した後、注文の進行を追跡するには、{{site.data.keyword.slportal}} から使用可能な [{{site.data.keyword.mdms_short}} 要求の詳細ページ](https://control.softlayer.com/storage/mdms){: external}を使用します。

以下の表は、{{site.data.keyword.mdms_short}} での要求の処理による注文状況の変化を示しています。

| 状況 | 説明 |
| --- | --- |
| 要求の処理中 (Processing Request) | {{site.data.keyword.mdms_short}} が要求を受信すると、状況が_「要求の処理中 (Processing request)」_に変わります。 |
| デバイスの準備中 (Prepping Device) | 注文が承認されると、要求の状況が_「デバイスの準備中 (Prepping Device)」_に変わります。 {{site.data.keyword.mdms_short}} は、次に使用可能なストレージ・デバイスを準備して構成します。  |
| 出荷待機中 (Awaiting Shipment) | 事前構成されたストレージ・デバイスが配送場所への出荷を待機しています。 要求が_「出荷待機中 (Awaiting shipment)」_状況になった注文は取り消すことができません。 |
| デバイスが発送されました (Device Shipped) | 配送業者がストレージ・デバイスを受け取り、配送場所に発送しました。 [要求の詳細ページ](https://control.softlayer.com/storage/mdms){: external}の_「注文の詳細 (Order Details)」_セクションで追跡番号を確認できます。 |
| デバイス受領済み (Device Received) | デバイスが {{site.data.keyword.cloud_notm}} に戻ると、状況が_「デバイス受領済み (Device Received)」_に変わります。 |
| データのオフロード中 (Offloading Data) | データ転送プロセス中は、要求の状況に_「データのオフロード中 (Offloading Data)」_と表示されます。 デバイスが {{site.data.keyword.cloud_notm}} データ・センター内のネットワークに接続され、データ・オフロードが自動的に開始されます。  |
| オフロード完了 (Offload Complete)| オフロード・プロセスが完了すると、要求の状況が_「オフロード完了 (Offload complete)」_に変わります。 これで、初期要求で指定したクラウド・オブジェクト・ストレージ宛先でデータが使用可能になりました。 |
| 消去完了 (Erase Complete) | {{site.data.keyword.mdms_short}} は、NIST のデータ・ワイプ規格を使用してデバイスからデータを完全に消去します。 データ消去プロセスが完了すると、注文の状況が_「消去完了 (Erase Complete)」_に変わります。
{: caption="表 1. {{site.data.keyword.mdms_short}} 注文状況ワークフローの説明" caption-side="top"}
