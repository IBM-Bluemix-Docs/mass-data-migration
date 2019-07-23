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

# 요청 관리
{: #manage-request}

{{site.data.keyword.slportal}}을 사용하여 {{site.data.keyword.mdms_full}} 주문의 상태를 관리하고 추적할 수 있습니다.
{: shortdesc}

{{site.data.keyword.mdms_short}} 베타 프로그램에 참여하면 {{site.data.keyword.cloud_notm}} 콘솔에서 액세스할 수 있는 새로운 {{site.data.keyword.mdms_short}} 서비스 대시보드를 미리 확인할 수 있습니다. 자세한 정보는 [베타에 액세스하기](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)를 참조하십시오.
{: tip}

## 주문 추적 
{: #track-order}

스토리지 디바이스를 요청한 후 {{site.data.keyword.slportal}}에서 사용 가능한 [{{site.data.keyword.mdms_short}} 요청 세부사항 페이지](https://control.softlayer.com/storage/mdms){: external}를 사용하여 주문의 진행상태를 추적할 수 있습니다. 

다음 표는 {{site.data.keyword.mdms_short}}에서 요청을 처리할 때 주문 상태가 어떻게 변경되는지를 보여줍니다. 

|상태 |설명 |
| --- | --- |
| 요청 처리 중 | {{site.data.keyword.mdms_short}}에서 요청을 수신하면 상태가 _요청 처리 중_으로 변경됩니다. |
| 디바이스 준비 중 | 주문이 승인되면 요청 상태가 _디바이스 준비 중_으로 변경됩니다. {{site.data.keyword.mdms_short}}에서 다음으로 사용 가능한 스토리지 디바이스를 준비하고 구성합니다. |
| 배송 대기 중 | 사전 구성된 스토리지 디바이스가 사용자의 위치로의 배송을 대기 중입니다. 요청이 _배송 대기 중_ 상태가 된 후에는 더 이상 주문을 취소할 수 없습니다. |
| 디바이스가 배송됨 | 스토리지 디바이스가 운송 업체를 통해 픽업되어 사용자의 위치로 배송되었습니다. 추적 번호는 [요청 세부사항 페이지](https://control.softlayer.com/storage/mdms){: external}의 _주문 세부사항_ 섹션에서 볼 수 있습니다. |
| 디바이스를 수령함 | 디바이스가 {{site.data.keyword.cloud_notm}}로 반환되면 상태가 _디바이스를 수령함_으로 변경됩니다. |
| 데이터 오프로드 중 | 데이터 전송 프로세스 중에는 요청 상태가 _데이터 오프로드 중_으로 표시됩니다. 디바이스가 {{site.data.keyword.cloud_notm}} 데이터 센터의 네트워크에 연결되고 데이터 오프로드가 자동으로 시작됩니다. |
| 오프로드 완료 | 오프로드 프로세스가 완료되면 요청 상태가 _오프로드 완료_로 변경됩니다. 이제 초기 요청에서 지정한 Cloud Object Storage 대상에서 데이터를 사용할 수 있습니다. |
| 지우기 완료 | {{site.data.keyword.mdms_short}}에서 NIST 데이터 지우기 표준을 사용하여 디바이스에서 데이터를 영구적으로 지웁니다. 데이터 지우기 프로세스가 완료된 후에는 주문 상태가 _지우기 완료_로 변경됩니다. {: caption="표 1. {{site.data.keyword.mdms_short}} 주문 상태 워크플로우 설명" caption-side="top"}
