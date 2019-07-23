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

# 사용 가능한 지역
{: #regions}

{{site.data.keyword.mdms_full}} 및 {{site.data.keyword.cos_full_notm}}를 사용할 경우 사용자의 가용성 및 복원성 필요에 맞는 다양한 스토리지 옵션 중에서 선택할 수 있습니다.   
{: shortdesc}

## 지원되는 지역
{: #available-regions}

{{site.data.keyword.mdms_short}} 디바이스는 미국(US), 유럽 연합(EU), 일본, 오스트레일리아, 브라질, 싱가포르, 홍콩, 노르웨이, 한국, 캐나다, 멕시코에서 주문할 수 있습니다. 

디바이스를 주문하기 전에 다음과 같은 배송 및 데이터 전송 제한사항에 유의하십시오. 

- **{{site.data.keyword.mdms_short}} 디바이스는 국경을 벗어나서 배송할 수 없습니다**. 단, EU 및 28개 소속 국가의 경우는 예외입니다. 예를 들어, 한 지역에 있는 디바이스로 데이터를 가져온 후 디바이스를 다른 지역으로 배송할 수는 없습니다. 
- **데이터는 소스 데이터가 상주하는 국가 내에서만 전송할 수 있습니다**. 단, EU 교차 지역 및 AP 교차 지역은 예외입니다. 즉, Cloud Object Storage 버킷 대상도 데이터 오프로드를 위해 {{site.data.keyword.mdms_short}} 디바이스를 스테이징할 데이터 센터와 동일한 국가에 있어야 합니다.  

## 스토리지 대상
{: #storage-destinations}

데이터는 Cloud Object Storage로 마이그레이션되는데, 이때 저장된 데이터에 대해 스토리지 클래스, 위치 및 복원성을 선택할 수 있습니다.  

{{site.data.keyword.mdms_short}}은 Cloud Object Storage에 사용할 수 있는 모든 저장 위치 및 복원성 옵션을 지원합니다. 다음 표에서는 사용 가능한 데이터 센터와 데이터 오프로드 옵션이 각 국가와 맵핑되어 있습니다. 

|국가 | 데이터 센터 | 스토리지 대상 |
|-----|-----|----|
|브라질 | 상파울루 | 단일 사이트: `sao01`  |
|캐나다 | 몬트리올 <br>토론토 | 단일 사이트: `mon01` <br>단일 사이트: `tor01` |
|멕시코| 멕시코 시티 | 단일 사이트: `mex01` |
|미국|Dallas<br> 산호세 <br>워싱턴 DC | 교차 지역: `us-geo`<br>지역: `us-south`<br>지역: `us-east`<br>단일 사이트: `sjc04` |
{: caption="표 1. 아메리카 대륙에서 사용 가능한 데이터 오프로드 위치" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers identify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-1}
{: tab-title="Americas"}
{: class="comparison-tab-table"}
{: row-headers}

|국가 | 데이터 센터 | 스토리지 대상 |
|-----|-----|----|
|Germany | 프랑크푸르트 | 교차 지역: `eu-geo`<br>지역: `eu-de`  | 
|이탈리아 | 밀라노 | 교차 지역: `eu-geo`<br>단일 사이트: `mil01`  | 
|네덜란드 | 암스테르담 | 교차 지역: `eu-geo`<br>단일 사이트: `ams03`| 
|노르웨이| 오슬로 | 교차 지역: `eu-geo`<br>단일 사이트: `oslo1`  | 
|영국 | 런던 | 교차 지역: `eu-geo`<br>지역: `eu-gb`  |
{: caption="표 2. 유럽에서 사용 가능한 데이터 오프로드 위치" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-2}
{: tab-title="Europe"}
{: class="comparison-tab-table"}
{: row-headers}

|국가 | 데이터 센터 | 스토리지 대상 |
|-----|-----|----|
|오스트레일리아 | 멜버른 <br>시드니 | 교차 지역: `ap-geo`<br>지역: `au-syd`<br>단일 사이트: `mel01`  |
|홍콩 |홍콩 | 교차 지역: `ap-geo`<br>단일 사이트: `hkg02`  |
|인도 | 첸나이 | 교차 지역: `ap-geo`<br>단일 사이트: `che01` | 
|일본 | 도쿄 | 교차 지역: `ap-geo`<br>지역: `jp-tok`  |
|한국| 서울 | 교차 지역: `ap-geo`<br>단일 사이트: `seo01`  | 
|싱가포르 |싱가포르 | 교차 지역: `ap-geo`| 
{: caption="표 3. 아시아 태평양에서 사용 가능한 데이터 오프로드 위치" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the service. The column headers indentify where that service is located. To understand where a service is located in the table, navigate to the row, and find the for the location you are interested in."}
{: #table-3}
{: tab-title="Asia Pacific"}
{: class="comparison-tab-table"}
{: row-headers}

스토리지 버킷 대상에 대한 자세한 정보는 [Cloud Object Storage 문서](/docs/services/cloud-object-storage/basics?topic=cloud-object-storage-endpoints)를 참조하십시오. 
