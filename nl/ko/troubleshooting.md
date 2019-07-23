---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# 문제점 해결
{: #troubleshooting}

{{site.data.keyword.mdms_full}} 사용과 관련된 일반 문제점에는 주문 상태 보기 또는 사용자 인터페이스 액세스가 포함될 수 있습니다. 대부분의 경우 몇 개의 간단한 단계를 수행하여 이러한 문제점을 복구할 수 있습니다.
{: shortdesc}

## SMB 공유에 연결할 수 없음
{: #unable-to-mount-smb-share}

{{site.data.keyword.mdms_short}} 디바이스에서 프로비저닝되는 SMB(Server Message Block) 공유를 마운트하려고 할 때 공유에 연결할 수 없습니다.  

Active Directory 도메인에 가입된 Windows 서버에서 SMB 파일 전송 프로토콜을 사용하고 있습니다. 데이터를 {{site.data.keyword.mdms_short}} 디바이스로 이동하려면 디바이스에서 프로비저닝되는 네트워크 공유에 연결해야 합니다. 디바이스의 10GbE 데이터 전송 포트에 해당하는 IP 주소에 대해 ping을 실행할 수 있지만, 서버에서 공유에 연결하거나 마운트할 수는 없습니다.
{: tsSymptoms}

{{site.data.keyword.mdms_short}} 디바이스를 Active Directory에 가입시키면 기본적으로 SMB 서명을 사용할 수 있습니다. SMB 서명을 사용하면 중간자 공격(man-in-the-middle attack) 발생 가능성이 없어지므로 네트워크 통신 중 보안이 강화됩니다. 그러나 SMB 서명은 데이터 전송 시 네트워크에 영향을 주거나 [공유를 서버에 마운트할 때 문제](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}를 유발할 수 있습니다.
{: tsCauses} 

사용자 환경에 SMB 서명이 필요하지 않거나 SMB 서명을 사용하지 않는 경우 클라이언트에서 SMB 서명을 사용 안함으로 설정하면 연결 문제를 방지하고 데이터 전송 성능을 높일 수 있습니다.
{: tsResolve}

Windows 서버에서 SMB 서명을 사용 안함으로 설정하려면 다음 레지스트리 키를 0으로 설정하십시오. 

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

SMB 서명에 대한 자세한 정보는 [SMB(Server Message Block) 서명 개요](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}를 참조하십시오. 

## 주문 세부사항을 볼 수 없음
{: #unable-to-view-order}

{{site.data.keyword.cloud_notm}} 콘솔에 액세스할 때 조직의 {{site.data.keyword.mdms_short}} 주문을 보거나 추적할 수 없습니다. 

{{site.data.keyword.cloud_notm}} 리소스 목록에 서비스 목록은 표시되지만, {{site.data.keyword.mdms_short}} 항목이 표시되지 않습니다.
{: tsSymptoms}

{{site.data.keyword.mdms_short}} 주문을 보거나 추적할 수 있는 올바른 권한이 없습니다.
{: tsCauses} 

해당 리소스 그룹 또는 서비스 인스턴스에서 올바른 역할을 지정받았는지 관리자에게 확인하십시오. 역할에 대한 자세한 정보는 [역할 및 권한](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles)을 참조하십시오.
{: tsResolve}

## 도움 및 지원 받기
{: #getting-help}

{{site.data.keyword.mdms_short}} 디바이스 사용 중에 문제 또는 문의사항이 있는 경우, 지원 센터에서 정보를 검색하거나 직접 연락하여 도움을 받을 수 있습니다. 

지원 센터에 액세스하려면 {{site.data.keyword.cloud_notm}} 콘솔에 로그인한 후 메뉴 표시줄에서 **지원**을 클릭하십시오. 

지원 센터 검색 필드를 사용하여 {{site.data.keyword.cloud_notm}} 문서 및 Stack Overflow 포럼에서 질문에 대한 답변을 찾을 수 있습니다. 지원 센터에서 지원 케이스를 관리할 수도 있습니다. Stack Overflow 포럼(기술 질문의 경우) 및 IBM Developer Answers 포럼(그 외의 모든 질문의 경우)에 대한 링크를 지원 센터의 포럼 섹션에서 찾을 수 있습니다. 

기본, 고급 또는 프리미엄 [지원 플랜](/docs/get-support?topic=get-support-support-plans#support-plans)을 사용하는 경우 지원을 받을 수 있는 전화번호 및 채팅 옵션을 찾을 수 있습니다. 

지원 센터가 지원을 받는 데 선호하는 방법이지만, {{site.data.keyword.cloud_notm}}에 로그인할 수 없는 경우에는 [{{site.data.keyword.cloud_notm}} 서비스 포털](http://www.ibm.biz/bluemixsupport){: external}을 사용하여 케이스를 제출할 수 있습니다. 

{{site.data.keyword.IBM_notm}} 지원 티켓 개설 및 지원 레벨과 티켓 심각도에 대한 자세한 정보는 [지원 센터에 문의](/docs/get-support?topic=get-support-getting-customer-support){: external}하십시오. 
