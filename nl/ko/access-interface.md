---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# 디바이스 사용자 인터페이스 액세스
{: #access-ui}

{{site.data.keyword.mdms_full}} 디바이스를 이더넷 연결에 사용하도록 구성한 후에는 디바이스 사용자 인터페이스에 액세스하여 디바이스와 상호작용하고 데이터 마이그레이션 프로세스를 시작할 수 있습니다.
{: shortdesc}

## 디바이스 인증 정보 검색(베타)
{: #retrieve-device-credentials}

사용자가 {{site.data.keyword.mdms_short}} 요청을 제출하면 이 서비스는 디바이스의 로컬 웹 UI에 액세스하는 데 사용할 수 있는 인증 정보를 사용자를 대신해 자동으로 생성합니다.  

이 기능은 [{{site.data.keyword.mdms_short}} 베타 릴리스](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)의 일부로 사용할 수 있습니다. [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}의 _요청 세부사항_ 섹션에서도 스토리지 디바이스에 대한 인증 정보에 액세스할 수 있습니다.
{: note}

디바이스 인증 정보를 검색하려면 다음을 수행하십시오. 

1. [{{site.data.keyword.cloud_notm}} 콘솔](https://{DomainName}/){: external}에 로그인하십시오. 
2. **메뉴** &gt; **리소스 목록**으로 이동하여 리소스 목록을 확인하십시오. 
3. {{site.data.keyword.cloud_notm}} 리소스 목록에서 {{site.data.keyword.mdms_short}}의 프로비저닝 인스턴스를 선택하십시오. 
4. _요청 세부사항_ 탭에서 인증 정보 섹션으로 이동하십시오. 
5. **사용자 이름** 및 **비밀번호** 값을 복사하십시오. 

## 디바이스 사용자 인터페이스에 로그인
{: #log-in-ui}

이전 단계에서 검색한 디바이스 인증 정보를 사용하여 로컬 웹 UI에 로그인한 후 {{site.data.keyword.mdms_short}} 디바이스와 상호작용하십시오. 

1. 웹 브라우저를 열고 주문 양식에 제공한 정적 IP 주소로 이동하십시오. 

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   `<device_management_IP_address>`를 Eth1 또는 Eth2 네트워크 포트에 대해 구성된 IP 주소로 대체하십시오. 인증서 예외를 허용하십시오.

2. 이전 단계에서 검색한 사용자 이름 및 비밀번호를 사용하여 디바이스 UI에 로그인하십시오.  

   ![로그인 페이지](images/login.png)
   
   공통 태스크 마법사가 표시됩니다. 왼쪽에서 오른쪽 순서로 옵션을 사용하여 데이터 가져오기를 시작하십시오. 

   ![워크플로우 아이콘](images/workflow.png)

   인터페이스의 왼쪽 상단에 있는 **워크플로우 관리자**를 사용하면 공통 태스크 마법사를 다시 열 수 있습니다.
   {:tip}

## 다음 단계
{: #access-ui-next-steps}

- 데이터 수집 복사를 준비하기 위해 먼저 [디바이스에서 스토리지 풀을 잠금 해제](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool)합니다. 
