---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: copy data to device, move data to device, 

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

# 디바이스로 데이터 복사
{: #copy-data}

디바이스 사용자 인터페이스를 사용하여 데이터를 {{site.data.keyword.mdms_full}} 디바이스로 복사할 수 있습니다. 

## 디바이스로 데이터 복사
{: #copy-data}

서버를 네트워크 공유에 연결한 후 디바이스로의 데이터 복사를 시작하고 모니터할 수 있습니다. 

1. 호스트 컴퓨터와 호환되는 파일 복사 도구를 사용하여 데이터를 네트워크 공유로 복사하십시오. 
2. 공통 태스크 마법사에서 **네트워크 활동 보기**를 클릭하여 데이터가 10Gb 링크에서 디바이스로 전송될 때의 인바운드 이더넷 로드를 표시하십시오. 
   
    ![활동 보기](images/NetworkPerf.png)
3. **스토리지 풀 보기**를 클릭하여 디바이스에서 스토리지 사용량 및 IOPS를 모니터하십시오. 
   
    ![스토리지 풀 보기](images/PoolPerf.png)

## 다음 단계
{: #import-data-next-steps}

- [디바이스를 정상 종료하십시오](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device). 
- 배송 레이블을 준비하고 [디바이스를 {{site.data.keyword.cloud_notm}}로 반환](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device)하십시오. 
