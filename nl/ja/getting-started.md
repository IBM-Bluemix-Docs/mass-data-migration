---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# 入門チュートリアル
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} は、テラバイト単位からペタバイト単位までのデータを {{site.data.keyword.cloud_notm}} に高速かつシンプルでセキュアな方法で移動するのに役立ちます。このチュートリアルでは、{{site.data.keyword.slportal}} を使用してマイグレーション・デバイスを要求する方法を示します。
{: shortdesc}

{{site.data.keyword.mdms_short}} の新しいフィーチャーに関心がありますか。{{site.data.keyword.mdms_short}} ベータ・プログラムに参加すると、今後のサービス拡張をプレビューできます。詳しくは、[ベータ版へのアクセス](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)を参照してください。
{: tip}

## 始める前に
{: #get-started-prereqs}

{{site.data.keyword.mdms_short}} デバイスを注文する前に、以下のことを行います。

- {{site.data.keyword.mdms_short}} が使用可能な[地域および場所](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions)を確認して、マイグレーションを計画します。
- {{site.data.keyword.cloud_notm}} アカウント用の [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} のインスタンスがプロビジョンされていることを確認します。 
- ご使用のネットワーク接続のタイプと速度を把握します。
- デバイスをソース・サーバーに接続するためのネットワーク設定 (IP アドレスやその他のルーティングの詳細など) を収集します。
- サイトでデバイスを受信、接続、および使用できるユーザーを特定します。

## ストレージ・バケットの作成
{: #get-started-create-bucket}

クラウド・オブジェクト・ストレージのインスタンスをプロビジョンした後、ストレージ・バケットを作成して、マイグレーションされたデータの宛先を設定します。 

1. {{site.data.keyword.cloud_notm}} リソース・リストでクラウド・オブジェクト・ストレージのプロビジョン済みインスタンスを選択します。
2. _「開始」_ページで**「バケットの作成」**をクリックします。
3. バケット名を入力し、データの回復力オプションを選択します。
   
   回復力オプションは、データがサービスにインポートされた後に、クラウド・オブジェクト・ストレージ・サービスによって地理的領域に分散される方法を決定します。 {{site.data.keyword.mdms_short}} は、クラウド・オブジェクト・ストレージで使用可能なすべての回復力オプションをサポートします。  
   {: note}
4. 場所のリストから、データをストレージ・バケットにマイグレーションした後に物理的に保管する地理的領域を選択します。
5. ストレージ・クラスのリストから**「標準」**を選択します。
6. **「バケットの作成」**をクリックします。

## デバイスの要求
{: #get-started-request-device}

{{site.data.keyword.mdms_short}} デバイスを要求するには、{{site.data.keyword.slportal}} を使用します。

1. [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} にログインします。
2. ナビゲーション・メニューから**「ストレージ」**>**「データ・マイグレーション」**>**「{{site.data.keyword.mdms_short}}」**をクリックして、{{site.data.keyword.mdms_short}} ランディング・ページにアクセスします。
3. **「デバイスの要求」**をクリックして、注文フォームを開きます。
4. 以下の詳細を指定して、{{site.data.keyword.mdms_short}} 要求を開始します。

    <table>
      <tr>
        <th>アクション</th>
        <th>説明</th>
      </tr>
      <tr>
        <td>要求名の追加</td>
        <td>{{site.data.keyword.mdms_short}} 要求を識別して追跡するための別名を入力します。</td>
      </tr>
      <tr>
        <td>データ・オフロードの宛先の選択</td>
        <td>ドロップダウン・リストからクラウド・オブジェクト・ストレージのプロビジョン済みインスタンスを選択します。 次に、マイグレーションしたデータを保管するストレージ・バケットに割り当てた名前を選択します。</td>
      </tr>
      <tr>
        <td>配送先住所の追加</td>
        <td>配送先住所やデリバリーを受け取る担当者の名前などの配送先情報を入力します。</td>
      </tr>
      <tr>
        <td>マイグレーション連絡先の追加</td>
        <td>デバイスへのデータ・マイグレーションを管理するユーザーの名前を入力します。</td>
      </tr>
      <tr>
        <td>ネットワーク設定の構成</td>
        <td>
          <p>ネットワーク構成の詳細を入力して、データ転送接続の設定を構成します。</p>
          <p>以下の<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">ネットワーク設定</a>を入力します。</p>
          <p>
            <ul>
              <li><i>デバイス管理の設定。</i> リモート・コンピューターの静的 IP アドレス、ネットマスク、およびデフォルト・ゲートウェイを入力します。</li>
              <li><i>データ転送の設定。</i> ソース・データがあるサーバーの静的 IP アドレスとネットマスクを入力します。</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">表 1. {{site.data.keyword.mdms_short}} 要求ワークフローの説明</caption>
    </table>

    デバイスの配送場所を選択するとき、デバイスの重量やアクセスのしやすさを考慮に入れてください。デバイスの重量は、そのハード・ケースおよびフォーム材輸送用ケース込みで約 27 kg (60 ポンド) になります。デバイスの配送に役立つように、輸送用ケースにはホイールとポップアップ・ハンドルが付いていて、簡単に移動できるようになっています。
    {: tip}
5. {{site.data.keyword.mdms_short}} サービス契約を読み、チェック・ボックスを選択します。
6. **「要求の送信 (Place Request)」**をクリックして、注文を完了します。 

## 次に行うこと
{: #get-started-next-steps}

完了しました。 {{site.data.keyword.mdms_short}} 要求がすべて設定されています。

- 注文の追跡について詳しくは、[要求の管理](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)を参照してください。
- デバイスの受け取りと接続について詳しくは、[デバイスのセットアップ](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview)を参照してください。

