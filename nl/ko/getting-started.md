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

# 시작하기 튜토리얼
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}}을 사용하면 테라바이트에서 페타바이트에 이르는 데이터를 빠르고 간단하며 안전한 방법으로 {{site.data.keyword.cloud_notm}}로 이동할 수 있습니다. 이 튜토리얼은 {{site.data.keyword.slportal}}을 통해 마이그레이션 디바이스를 요청하는 방법에 대해 설명합니다.
{: shortdesc}

{{site.data.keyword.mdms_short}}의 새로운 기능을 사용해 보고 싶으십니까? {{site.data.keyword.mdms_short}} 베타 프로그램에 참여하면 예정된 서비스 개선사항을 미리 확인할 수 있습니다. 자세한 정보는 [베타에 액세스하기](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)를 참조하십시오.
{: tip}

## 시작하기 전에
{: #get-started-prereqs}

{{site.data.keyword.mdms_short}} 디바이스를 주문하기 전에 다음을 수행하십시오. 

- {{site.data.keyword.mdms_short}}이 제공되는 [지역 및 위치](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions)를 검토하여 마이그레이션 계획을 세우십시오. 
- {{site.data.keyword.cloud_notm}} 계정에 해당하는 [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external}의 프로비저닝 인스턴스가 있는지 확인하십시오.  
- 네트워크 연결 유형과 속도를 이해합니다. 
- 디바이스를 소스 서버에 연결하는 데 필요한 IP 주소 및 기타 라우팅 세부사항과 같은 네트워크 설정을 수집하십시오. 
- 현장에서 디바이스를 수령, 연결 및 사용할 수 있는 사람을 식별하십시오. 

## 스토리지 버킷 작성
{: #get-started-create-bucket}

Cloud Object Storage의 인스턴스를 프로비저닝한 후 스토리지 버킷을 작성하여 마이그레이션된 데이터의 대상을 설정하십시오.  

1. {{site.data.keyword.cloud_notm}} 리소스 목록에서 Cloud Object Storage의 프로비저닝 인스턴스를 선택하십시오. 
2. _시작하기_ 페이지에서 **버킷 작성**을 클릭하십시오. 
3. 버킷 이름을 입력하고 데이터에 대한 복원성 옵션을 선택하십시오. 
   
   복원성 옵션은 데이터를 서비스로 가져온 후 Cloud Object Storage 서비스를 통해 데이터가 지역 전반에 분배되는 방식을 결정합니다. {{site.data.keyword.mdms_short}}은 Cloud Object Storage에 사용할 수 있는 모든 복원성 옵션을 지원합니다.   
   {: note}
4. 데이터가 스토리지 버킷으로 마이그레이션된 후 데이터를 실제로 저장할 지역을 위치 목록에서 선택하십시오. 
5. 스토리지 클래스 목록에서 **표준**을 선택하십시오. 
6. **버킷 작성**을 클릭하십시오. 

## 디바이스 요청
{: #get-started-request-device}

{{site.data.keyword.slportal}}을 사용하여 {{site.data.keyword.mdms_short}} 디바이스를 요청할 수 있습니다. 

1. [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}에 로그인하십시오. 
2. 탐색 메뉴에서 **스토리지** > **데이터 마이그레이션** > **{{site.data.keyword.mdms_short}}**을 클릭하여 {{site.data.keyword.mdms_short}} 시작 페이지를 클릭하십시오. 
3. **디바이스 요청**을 클릭하여 주문 양식을 여십시오.
4. 다음 세부사항을 지정하여 {{site.data.keyword.mdms_short}} 요청을 시작하십시오. 

    <table>
      <tr>
        <th>조치</th>
        <th>설명</th>
      </tr>
      <tr>
        <td>요청 이름 추가</td>
        <td>{{site.data.keyword.mdms_short}} 요청을 식별하고 추적하기 위한 별명을 입력하십시오. </td>
      </tr>
      <tr>
        <td>데이터 오프로드 대상 선택</td>
        <td>드롭 다운 목록에서 Cloud Object Storage의 프로비저닝 인스턴스를 선택하십시오. 그런 다음 마이그레이션된 데이터를 저장할 스토리지 버킷에 지정한 이름을 선택하십시오. </td>
      </tr>
      <tr>
        <td>배송 주소 추가</td>
        <td>배송 주소 및 배송 승인자의 이름과 같은 배송 정보를 입력하십시오. </td>
      </tr>
      <tr>
        <td>마이그레이션 담당자 추가</td>
        <td>디바이스로의 데이터 마이그레이션을 관리할 사람의 이름을 입력하십시오. </td>
      </tr>
      <tr>
        <td>네트워크 설정 구성</td>
        <td>
          <p>네트워크 구성 세부사항을 입력하여 데이터 전송 연결 설정을 구성하십시오. </p>
          <p>다음 <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">네트워크 설정</a>을 제공하십시오. </p>
          <p>
            <ul>
              <li><i>디바이스 관리 설정</i> - 원격 컴퓨터의 정적 IP 주소, 넷마스크, 기본 게이트웨이를 입력하십시오. </li>
              <li><i>데이터 전송 설정</i> - 소스 데이터가 상주하는 서버의 정적 IP 주소 및 넷마스크를 입력하십시오. </li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">표 1. {{site.data.keyword.mdms_short}} 요청 워크플로우 설명</caption>
    </table>

    디바이스 배송 위치를 선택할 때 디바이스의 중량과 접근성을 고려하십시오. 하드 케이스 및 폼 여행용 케이스를 포함한 디바이스의 중량은 약 60파운드입니다. 디바이스 운반을 돕기 위해 여행용 케이스에는 쉽게 조작할 수 있도록 바퀴와 팝업 핸들이 장착되어 있습니다.
    {: tip}
5. {{site.data.keyword.mdms_short}} 서비스 계약을 읽은 후 선택란을 선택하십시오. 
6. **요청 제출**을 클릭하여 주문을 완료하십시오.  

## 다음에 수행할 작업
{: #get-started-next-steps}

성공했습니다! {{site.data.keyword.mdms_short}} 요청이 모두 설정되었습니다. 

- 주문 추적에 대한 자세한 정보는 [요청 관리](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)를 확인하십시오. 
- 디바이스 수령 및 연결에 대한 자세한 정보는 [디바이스 설정](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview)을 확인하십시오. 

