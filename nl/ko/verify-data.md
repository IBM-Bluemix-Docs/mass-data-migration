---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# 데이터 확인
{: #verify-data}

{{site.data.keyword.cos_full}}를 사용하여 마이그레이션된 데이터에 액세스하여 이 데이터를 확인할 수 있습니다.
{: shortdesc}

오프로드가 완료되면 {{site.data.keyword.cloud_notm}}에서 디바이스를 안전하게 지우는 동안 클라우드에 있는 데이터에 즉시 액세스할 수 있습니다. 

## Cloud Object Storage에서 데이터 액세스
{: #access-data-cos}

마이그레이션된 데이터는 {{site.data.keyword.mdms_short}} 요청을 제출할 때 지정한 Cloud Object Storage 인스턴스에서 사용할 수 있습니다. 소스 서버에서 데이터를 삭제하기 전에 데이터가 {{site.data.keyword.cloud_notm}}에 성공적으로 업로드되었는지 확인하십시오. 

데이터에 액세스하여 데이터를 확인하려면 다음을 수행하십시오.  

1. [{{site.data.keyword.cloud_notm}} 콘솔](https://{DomainName}/){: external}에 로그인하십시오. 
2. **메뉴** &gt; **리소스 목록**으로 이동하여 리소스 목록을 확인하십시오. 
3. {{site.data.keyword.cloud_notm}} 리소스 목록에서 Cloud Object Storage의 프로비저닝 인스턴스를 선택하십시오. 
4. 사용 가능한 스토리지 버킷 목록에서 데이터 마이그레이션용으로 지정한 버킷 이름을 선택하십시오. 
5. 버킷과 연관된 오브젝트가 {{site.data.keyword.mdms_short}} 디바이스로 복사한 데이터와 일치하는지 확인하십시오. 

## 다른 스토리지 솔루션으로 데이터 이동
{: #move-data}

워크로드 요구사항에 따라 Cloud Object Storage의 마이그레이션된 데이터를 [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) 또는 [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage)와 같은 다른 클라우드 스토리지 솔루션으로 이동해야 할 수도 있습니다.  

스토리지 마이그레이션 옵션에 대한 자세한 정보는 [레시피: File 또는 Block Storage에서 COS로 데이터 이동](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}을 참조하십시오. 

