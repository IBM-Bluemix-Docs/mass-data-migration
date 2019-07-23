---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# FAQ
{: #faqs}

{{site.data.keyword.mdms_full}} に関するよくある質問。
{: shortdesc}

## {{site.data.keyword.mdms_full_notm}} とは何ですか。
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} は、120 TB の使用可能容量がある堅牢なポータブル・ストレージ・デバイスを使用して、テラバイト単位からペタバイト単位までのデータを {{site.data.keyword.cloud_notm}} に安全に移動する処理を加速する物理データ転送サービスです。

## {{site.data.keyword.mdms_short}} の使用を開始するにはどうすればよいですか。
{: #how-to-use-mdms}
{: faq}

[{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} を使用して要求を送信してください。 要求が承認され、処理が行われると、ネットワーク情報と配送先情報に基づいて次に利用可能なデバイスの構成が行われて、デバイスが配送されます。  

## {{site.data.keyword.mdms_short}} は誰が使用しますか。
{: #who-uses-mdms}
{: faq}

データ・センターやオフィスから、石油掘削装置や船舶などのリモート・ロケーションにいたるまで、{{site.data.keyword.mdms_short}} デバイスはほぼすべての環境で実行するための装備を備えています。 コストや処理速度の点でネットワーク経由のデータ転送オプションが望ましくない場合や、そのようなオプションが利用できない場合にも、{{site.data.keyword.mdms_short}} を代替手段として活用できます。

## {{site.data.keyword.mdms_short}} を使用してどれくらいの量のデータを転送できますか。
{: #how-much-data}
{: faq}

数テラバイトであっても、何百ペタバイトであっても、転送可能なデータ量には実質的に制限がありません。 1 台のデバイスの使用可能な容量は最大 120 TB ですが (RAID-6)、それを超えたワークロードにも複数のデバイスを使用して対応できます。 {{site.data.keyword.mdms_short}} はインライン圧縮も提供します。これにより、データ・セットの圧縮によっては、さらに使用可能な容量が増える可能性があります。 単一オブジェクトの最大サイズは 10 TB に制限されています。


## 複数のデバイスを使用して、120 TB を超える大規模なワークロードを移動するにはどのようにしますか。
{: #using-multiple-devices}
{: faq}

複数のデバイスを並列または直列で使用して、すべてのデータを 1 回のマイグレーションで移動することも、1 台のデバイスでマイグレーションを反復的に実行することもできます。 例えば、1 PB のデータ転送に 9 台のデバイスを並列で使用することも、1 台のデバイスを使用してマイグレーションを 9 回実行することもできます。 複数のデバイスを並列で使用する場合は、取り込み速度が遅くなることに注意してください。

## データの転送にはどのくらいの時間がかかりますか。
{: #transfer-timeline}
{: faq}

お客様が {{site.data.keyword.mdms_short}} 要求を送信してから、IBM Cloud Object Storage バケットでデータがアクセス可能になるまでのターンアラウンド・タイムは、数日程度です。 転送パフォーマンスは、ネットワーキング、帯域幅、転送されるファイル数などの多くの要因の影響を受ける可能性があります。 例えば、数百万個の小さなファイルを転送するときは、比較的少数の、より大きいファイルに同じ量のデータを入れて転送するときより長い時間がかかります。

## {{site.data.keyword.mdms_short}} デバイスを使用できる期間はどれくらいですか。
{: #device-onsite-time}
{: faq}

最初の 10 営業日の間、追加コストなしでデバイスをオンサイトに置いておくことができます。 これには、デバイスが出荷される日や、デバイスが IBM に返却される日 (最大 2 日) は含まれません。 データの取り込みにさらに時間が必要な場合は、それ以降の 1 暦日あたり 30 USD で使用期間を延長できます。これはすべての地域に適用されます。

## {{site.data.keyword.mdms_short}} では、どのようなネットワーク・インターフェースがサポートされますか。
{: #supported-network-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} デバイスには、10 Gbps のネットワーク・インターフェースと、RJ45 (CAT6a) と SFP+ 銅線に対応したネットワーク・ポートがあります。

RJ45 から SFP+ へのコンバーターは、SFP+ ネイティブ接続がないデバイス・モデルにのみ組み込まれています。 ファイバーは現時点ではサポートされていません。

## {{site.data.keyword.mdms_short}} のデフォルトの配送オプションはどういうものですか。
{: #shipping-options}
{: faq}

すべての {{site.data.keyword.mdms_short}} デバイスで、UPS Next Day Air の往復配送を利用します。 配送料は、デバイス 1 台あたり 395 USD という均一の低料金の中に含まれています。 現在は、お客様が別の配送方法を選択することはできません。


## {{site.data.keyword.mdms_short}} はどの地域で使用可能ですか。
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}} は、現在、米国 (US)、EU、日本、オーストラリア、ブラジル、シンガポール、香港、ノルウェー、韓国、カナダ、およびメキシコで使用可能です。 さらに地理的な拡張が行われています。 オンライン・オーダーはほとんどの地域で使用できます。 地域でオンライン・オーダーを使用できない場合は、サービスの使用について IBM 営業担当員にお問い合わせください。

EU とその 28 加盟国を除き、デバイスを国境を越えて配送することはできません (例えば、ある地域でデバイスを注文して別の地域に配送することはできません)。
{: note}

## 米国内での {{site.data.keyword.mdms_short}} のデフォルトの配送オプションはどういうものですか。
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}} は、米国のデバイスには UPS Overnight Shipping の往復配送を使用します。 配送コストは料金に含まれます。 現在は、お客様が別の配送方法を選択することはできません。 

## EU 内での {{site.data.keyword.mdms_short}} のデフォルトの配送オプションはどういうものですか。
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}} は、EU のデバイスには FedEx Overnight Shipping の往復配送を使用します。 配送コストは料金に含まれます。 現在は、お客様が別の配送方法を選択することはできません。 

## サポートされるその他すべての地域での {{site.data.keyword.mdms_short}} のデフォルトの配送オプションはどういうものですか。
{: #default-shipping-other}
{: faq}

米国および EU 以外のサポートされるすべての地域では、配送ベンダーと配送ターンアラウンド・タイムが異なります。 配送コストは料金に含まれます。 現在は、お客様が別の配送方法を選択することはできません。

これらの地域では、発注時に IBM が往復配送を予約することができません。 代わりに、配送が必要になった時点で、片道配送が予約されます。 出荷については、要求後に IBM が {{site.data.keyword.mdms_short}} デバイスの配送を調整するため、少なくとも 3 営業日を見越してください。
{: note}

米国や EU 以外の注文の場合、デバイスを配送する日付の 3 営業日以上前にデバイスの返品配送を要求します。 例えば、金曜日にデバイスを出荷する場合は、同じ週の月曜日に返品配送を調整します。 返品配送は、{{site.data.keyword.mdms_short}} ダッシュボードの_「要求の詳細」_タブから要求できます。
{: important}

## 日本、オーストラリア、ブラジル、カナダ、メキシコ、香港、シンガポール、ノルウェー、または韓国にいる場合、 {{site.data.keyword.mdms_short}} デバイスの返品配送を要求するにはどうすればよいですか。
{: #shipping-timetable-other}
{: faq}

{{site.data.keyword.mdms_short}} を米国および EU 以外の地域で使用している場合は、デバイスを出荷する日付の 3 営業日以前に返品配送を要求する必要があります。 例えば、金曜日にデバイスを出荷する場合は、同じ週の月曜日に返品配送を調整します。 

## データを {{site.data.keyword.cloud_notm}} にインポートするためにどの程度の費用がかかりますか。
{: #data-transfer-cost}
{: faq}

{{site.data.keyword.cloud_notm}} へのデータ転送は無料です。


## {{site.data.keyword.mdms_short}} を使用して、{{site.data.keyword.cloud_notm}} からデータをエクスポートできますか。
{: #exporting-data}
{: faq}

{{site.data.keyword.mdms_short}} は、現時点では、{{site.data.keyword.cloud_notm}} からのデータのエクスポートをサポートしていません。


## {{site.data.keyword.mdms_short}} ではデータが暗号化されますか。
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}} では、すべてのデータが AES 256 ビットで暗号化されます。強力なパスワードでストレージ・プールのロックを解除する機能もあります。 {{site.data.keyword.IBM}} では、すべてのデータ転送が SSL で行われます。

## {{site.data.keyword.mdms_short}} の物理的な面でのデータ保護はどうなっていますか。
{: #security}
{: faq}

すべての {{site.data.keyword.mdms_short}} デバイスは、頑丈で耐久性のある筐体に収納されています。 この収納ケースは、耐水設計、耐衝撃設計、改ざんの証拠を残す設計になっていて、配送の往復時にもデバイスとデータのセキュリティーが確保されています。

## マイグレーション・プロセス全体で要求をどのように追跡できますか。
{: #how-to-track-request}
{: faq}

要求の状況を追跡するには、{{site.data.keyword.cloud_notm}} コンソールの {{site.data.keyword.mdms_short}} ダッシュボードで_「要求の詳細」_タブにナビゲートします。

## データが {{site.data.keyword.cos_full_notm}} にオフロードされた後に、どのように {{site.data.keyword.mdms_short}} デバイスからデータを消去しますか。
{: #data-erasure}
{: faq}

IBM Cloud Object Storage にデータをオフロードするとすぐに、IBM は NIST のデータ・ワイプ規格を使用してデバイスを消去し、確実にデバイスからすべてのクライアント・データを完全に消去します。

## {{site.data.keyword.mdms_short}} のファイル・インターフェースは何ですか。
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} では、ネットワーク・ファイル・システム (NFS) プロトコルと Server Message Block (SMB) プロトコルがサポートされます。

## {{site.data.keyword.mdms_short}} のファイル・インターフェースを使用するにはどうすればよいですか。
{: #how-to-use-file-interface}
{: faq}

最初に、暗号化プールのロックを解除します。 その後、マイグレーションするデータが入っているサーバーに共有をマウントします。 ネットワーク共有にデータ・ファイルをコピーする操作を開始します。

## {{site.data.keyword.mdms_short}} のファイル・インターフェースには、どのようなメリットがありますか。
{: #file-interface-benefits}
{: faq}

このファイル・インターフェースは、安定したファイル/ネットワーク・ソフトウェアに基づいているので、多数の巨大なファイルをコピーして {{site.data.keyword.cloud_notm}} に転送できます。

## {{site.data.keyword.mdms_short}} デバイスではファイルがどのように保管されますか。
{: #file-storage}
{: faq}

{{site.data.keyword.mdms_short}} デバイスでは、LZ4 圧縮と AES 256 ビット暗号化を備えた ZFS ファイル・システムを使用します。

## 米国の場合、{{site.data.keyword.mdms_short}} の使用料はいくらですか。
{: #pricing-us}
{: faq}

米国では、デバイス 1 台あたり 395 USD という均一料金になっています。この内訳は、デバイス料金が 295 USD、UPS Overnight Shipping の往復配送料が 100 USD です。この料金で、10 営業日の間、お客様のサイトでご利用になれます。

10 日のオンサイトでの使用期間には、デバイスが出荷される日や、デバイスが IBM に返却される日 (最大 2 日) は含まれません。 マイグレーションに割り当てられた 10 営業日を超える時間が必要な場合は、使用日数を 1 日追加するごとに 1 日あたり 30 USD の延長料金がかかります。

## EU の場合、{{site.data.keyword.mdms_short}} の使用料はいくらですか。
{: #pricing-eu}
{: faq}

EU では、デバイス 1 台あたり 445 USD という均一料金になっています。この内訳は、デバイス料金が 295 USD、FedEx Overnight Shipping の往復配送料が 150 USD です。この料金で、10 営業日の間、お客様のサイトでご利用になれます。

10 日のオンサイトでの使用期間には、デバイスが出荷される日や、デバイスが IBM に返却される日 (最大 2 日) は含まれません。 マイグレーションに割り当てられた 10 日を超える時間が必要な場合は、使用日数を 1 日追加するごとに 1 日あたり 30 USD の延長料金がかかります。

## その他すべてのサポートされる地域の場合、{{site.data.keyword.mdms_short}} の使用料はいくらですか。
{: #pricing-other}
{: faq}

その他すべての地域 (日本、オーストラリア、ブラジル、カナダ、メキシコ、香港、シンガポール、ノルウェー、および韓国) では、デバイス 1 台あたり 1,145 USD という均一料金になっています。この内訳は、デバイス料金が 295 USD、往復配送料が 850 USD です。この料金で、10 営業日の間、お客様のサイトでご利用になれます。

10 日のオンサイトでの使用期間には、デバイスが出荷される日や、デバイスが IBM に返却される日 (最大 2 日) は含まれません。 マイグレーションに割り当てられた 10 日を超える時間が必要な場合は、使用日数を 1 日追加するごとに 1 日あたり 30 USD の延長料金がかかります。

これらの地域には特別な配送要件があります。 詳しくは、上記を参照してください。
{: note}

## {{site.data.keyword.cos_full_notm}} 使用時に課金されますか。
{: #pricing-cos}
{: faq}

{{site.data.keyword.cloud_notm}} へのデータ転送は無料です。ただし、{{site.data.keyword.cos_full_notm}} や他の {{site.data.keyword.cloud_notm}} サービスでデータを保管するための標準料金が発生します。 クラウド・オブジェクト・ストレージの価格設定オプションについて詳しくは、[{{site.data.keyword.cos_full_notm}} の料金設定](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}を参照してください。 

## {{site.data.keyword.mdms_full_notm}} デバイスを購入できますか。
{: #purchasing-devices}
{: faq}

{{site.data.keyword.mdms_full_notm}} デバイスは販売されていません。

## {{site.data.keyword.mdms_short}} のプロセスで、オブジェクト名の固有性はどのように維持されますか。
{: #object-name-uniqueness}
{: faq}

オブジェクトがクラウド・オブジェクト・ストレージ・バケットにコピーされるとき、オブジェクト名の固有性を確保するために、ファイル・パスがプレフィックスとしてオブジェクト名に組み込まれます。 例えば、`/root/user/config.ini` がバケットにコピーされると、`root/user/config.ini` になります。

## {{site.data.keyword.cos_full_notm}} アカウントにターゲット・バケットが存在しない場合はどうなりますか。
{: #target-buckets}
{: faq}

ターゲット・バケットが存在しない場合は、作成されます。 存在する場合は、空のバケットでなければなりません。空でないと、コピー処理ができません。  

## スキャン・プロセス中にリンクはスキップされますか?
{: #links-scan-process}
{: faq}

はい。 スキャン・プロセス中に、シンボリック・リンクとハード・リンクはスキップされます。
