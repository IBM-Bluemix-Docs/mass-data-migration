---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: region availability, storage locations, storage destinations

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

# 使用可能な地域
{: #regions}

{{site.data.keyword.mdms_full}} と {{site.data.keyword.cos_full_notm}} を使用すると、可用性と回復力のニーズを満たすさまざまなストレージ・オプションから選択できます。  
{: shortdesc}

## サポートされる地域
{: #available-regions}

{{site.data.keyword.mdms_short}} デバイスは、米国 (US)、欧州連合 (EU)、日本、オーストラリア、ブラジル、シンガポール、香港、ノルウェー、韓国、カナダ、メキシコで注文できます。

デバイスを注文する前に、配送およびデータ転送についての以下の制約事項に留意してください。

- **{{site.data.keyword.mdms_short}} デバイスは、国境を越えて配送することはできません** (EU およびその 28 の加盟国を除く)。例えば、ある地域でデバイスにデータをインポートしてから、そのデバイスを別の地域に配送することはできません。
- **ソース・データがある国内でのみデータを転送できます** (EU 地域間および AP 地域間を除く)。これは、データ・オフロードのために {{site.data.keyword.mdms_short}} デバイスがステージングされるデータ・センターと同じ国内に Cloud Object Storage バケットの宛先もなければならないことを意味します。 

## ストレージの宛先
{: #storage-destinations}

データは Cloud Object Storage にマイグレーションされ、保管されるデータに対してさまざまなストレージ・クラス、ロケーション、および回復力を選択できます。 

{{site.data.keyword.mdms_short}} では、Cloud Object Storage で使用可能なすべてのストレージ・ロケーションおよび回復力オプションがサポートされます。以下の表に、各国の使用可能なデータ・センターとデータ・オフロード・オプションを示します。

| 国 | データ・センター | ストレージの宛先 |
|-----|-----|----|
| ブラジル | サンパウロ | 単一サイト: `sao01`  |
| カナダ | モントリオール<br>トロント | 単一サイト: `mon01` <br>単一サイト: `tor01` |
| メキシコ| メキシコ・シティー | 単一サイト: `mex01` |
| 米国|  ダラス<br>サンノゼ<br>ワシントン DC | 地域間: `us-geo`<br>地域: `us-south`<br>地域: `us-east`<br>単一サイト: `sjc04` |
{: caption="表 1. アメリカで使用可能なデータ・オフロード・ロケーションのリスト" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

| 国 | データ・センター | ストレージの宛先 |
|-----|-----|----|
| ドイツ | フランクフルト | 地域間: `eu-geo`<br>地域: `eu-de`  | 
| イタリア | ミラノ | 地域間: `eu-geo`<br>単一サイト: `mil01`  | 
| オランダ | アムステルダム | 地域間: `eu-geo`<br>単一サイト: `ams03`| 
| ノルウェー| オスロ | 地域間: `eu-geo`<br>単一サイト: `oslo1`  | 
| 英国 | ロンドン | 地域間: `eu-geo`<br>地域: `eu-gb`  |
{: caption="表 2. ヨーロッパで使用可能なデータ・オフロード・ロケーションのリスト" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

| 国 | データ・センター | ストレージの宛先 |
|-----|-----|----|
| オーストラリア | メルボルン<br>シドニー |  地域間: `ap-geo`<br>地域: `au-syd`<br>単一サイト: `mel01`  |
| 香港 | 香港 | 地域間: `ap-geo`<br>単一サイト: `hkg02`  |
| インド | チェンナイ | 地域間: `ap-geo`<br>単一サイト: `che01` | 
| 日本 | 東京 | 地域間: `ap-geo`<br>地域: `jp-tok`  |
| 韓国| ソウル | 地域間: `ap-geo`<br>単一サイト: `seo01`  | 
| シンガポール | シンガポール | 地域間: `ap-geo` | 
{: caption="表 3. アジア太平洋で使用可能なデータ・オフロード・ロケーションのリスト" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

ストレージ・バケット宛先について詳しくは、[Cloud Object Storage の資料](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints)を参照してください。
