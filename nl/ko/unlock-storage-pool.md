---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# 스토리지 풀 잠금 해제
{: #unlock-storage-pool}

디바이스에 대해 프로비저닝된 스토리지 풀을 먼저 잠금 해제하고 활성화하여 데이터를 {{site.data.keyword.mdms_full}} 디바이스로 복사할 수 있습니다.
{: shortdesc}

## 스토리지 풀 비밀번호 문구 검색(베타)
{: #retrieve-storage-pool-passcode}

{{site.data.keyword.mdms_short}} 디바이스에서 스토리지 풀에 액세스하려면 {{site.data.keyword.cloud_notm}} 콘솔에서 {{site.data.keyword.mdms_short}} 요청 세부사항으로 이동하여 디바이스 인증 정보를 검색하십시오. 

이 기능은 [{{site.data.keyword.mdms_short}} 베타 릴리스](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta)의 일부로 사용할 수 있습니다. [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}의 _요청 세부사항_ 섹션에서도 스토리지 디바이스에 대한 인증 정보에 액세스할 수 있습니다.
{: note}

스토리지 풀 비밀번호 문구를 검색하려면 다음을 수행하십시오. 

1. [{{site.data.keyword.cloud_notm}} 콘솔](https://{DomainName}/){: external}에 로그인하십시오. 
2. **메뉴** &gt; **리소스 목록**으로 이동하여 리소스 목록을 확인하십시오. 
3. {{site.data.keyword.cloud_notm}} 리소스 목록에서 {{site.data.keyword.mdms_short}}의 프로비저닝 인스턴스를 선택하십시오. 
4. _요청 세부사항_ 탭에서 인증 정보 섹션으로 이동하십시오. 
5. **풀 잠금 패스코드** 값을 복사하십시오. 

## 스토리지 풀 활성화
{: #activate-storage-pool}

이전 단계에서 검색한 인증 정보를 사용하여 빈 스토리지 풀을 잠금 해제하십시오. 

1. [디바이스 사용자 인터페이스에 로그인하십시오](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui). 
2. 공통 태스크 마법사에서 **스토리지 풀 잠금 해제 및 시작**을 클릭하십시오. 
3. 1단계에서 검색한 스토리지 풀 비밀번호 문구를 입력한 후 **확인**을 클릭하십시오. 
      
   ![스토리지 풀 활성화](/images/StartStoragePool.png)

   기본적으로 공유에서는 NFS(Network File System) 및 SMB(Server Message Block) 프로토콜이 모두 액세스 제한 없이 사용 가능합니다. 사용자 인터페이스에서 공유 이름을 마우스 오른쪽 단추로 클릭한 후 해당 메뉴 옵션을 선택하여 NFS 또는 SMB용으로 이 공유에 대한 액세스를 수정할 수 있습니다.
   {: note}

## 다음 단계
{: #unlock-storage-pool-next-steps}

- Unix 시스템을 사용 중인 경우 [NFS를 사용하여 네트워크 공유에 연결](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share)하십시오. 
- Windows 시스템을 사용 중인 경우 [SMB를 사용하여 네트워크 공유에 연결](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share)하십시오. 
- [데이터 복사 프로세스](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy)를 시작하십시오. 
