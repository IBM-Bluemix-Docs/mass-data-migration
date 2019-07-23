---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# デバイスの返却
{: #return-device}

{{site.data.keyword.mdms_full}} デバイスの電源を遮断し、{{site.data.keyword.cloud_notm}} に返却して、マイグレーション・プロセスを完了します。
{: shortdesc}

## デバイスの切断
{: #disconnect-device}

データ・コピー・プロセスが完了した後、システムの電源を正常にオフにすることができます。

1. 「共通タスク」ウィザードで、**「アプライアンスのシャットダウン (Shutdown Appliance)」**をクリックします。

    ![アプライアンスのシャットダウン](images/ShutDown.png)

    **「OK」**をクリックして確認します。
2. デバイスの **System On / Off** ボタンを使用して、デバイスの電源をオフにします。 
3. **Mains スイッチ**を**オフ**に設定します。
4. すべてのケーブルと光部品を巻き取り、輸送用ケース内の保管場所に戻します。

## {{site.data.keyword.cloud_notm}} へのデバイスの配送
{: #ship-device}

デバイスを返却する準備ができたら、配送ラベルを準備し、配送業者に連絡します。

1. デバイスの品目リストと返却配送ラベルを取り出します。これらの文書は、輸送用ケースの蓋の下にあります。

    複数のデバイスを配送する場合は、各ケースに入っている返却配送ラベルはストレージ・デバイスに固有であることに注意してください。配送業者の集荷を手配する前に、対応する返却配送ラベルが該当するデバイスに貼られていることを確認してください。
    {: note}
2. 品目リストを使用して、すべてのケーブルと光部品が輸送用ケースに戻されて格納されていることを確認します。
3. 品目リストを輸送用ケースに戻してから、返却配送ラベルに記載されている説明に従ってラベルをデバイスに貼り付けます。
4. 配送業者の集荷を手配し、デバイスをデータ・センターに返却します。

    デバイスが {{site.data.keyword.cloud_notm}} に返却されると、{{site.data.keyword.mdms_short}} 要求の詳細ページの注文状況が_「デバイス受領済み (Device received)」_に変わります。

## 次のステップ
{: #return-device-next-steps}

- [{{site.data.keyword.mdms_short}} 要求を管理](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)して、注文の状況を確認します。
- ソース・サーバーからデータを削除する前に、[データが {{site.data.keyword.cloud_notm}} に正常にアップロードされたことを確認します](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data)。

