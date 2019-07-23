---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# 디바이스 반환
{: #return-device}

{{site.data.keyword.mdms_full}} 디바이스의 전원을 끄고 {{site.data.keyword.cloud_notm}}로 반환하면 마이그레이션 프로세스가 완료됩니다.
{: shortdesc}

## 디바이스 연결 해제
{: #disconnect-device}

데이터 복사 프로세스가 완료되면 시스템 전원을 정상적으로 끌 수 있습니다. 

1. 공통 태스크 마법사에서 **어플라이언스 종료**를 클릭하십시오. 

    ![어플라이언스 종료](images/ShutDown.png)

     **확인**을 클릭하여 확인하십시오.
2. 디바이스의 **시스템 켜기/끄기** 단추를 사용하여 디바이스의 전원을 끄십시오.  
3. **주 스위치**를 **꺼짐**으로 설정하십시오. 
4. 모든 케이블과 광학장치를 되감아서 운송용 케이스 내부의 보관 위치에 집어넣으십시오. 

## {{site.data.keyword.cloud_notm}}로 디바이스 반환
{: #ship-device}

디바이스를 반환할 준비가 되었으면 배송 레이블을 준비하고 운송 업체에 알리십시오. 

1. 디바이스의 인벤토리 목록 및 반송 레이블을 검색하십시오. 이러한 문서는 운송용 케이스의 덮개에 있습니다. 

    디바이스를 여러 개 배송하는 경우에는 각 케이스에 제공된 반송 레이블이 스토리지 디바이스에 따라 다릅니다. 운송 업체와 픽업 스케줄을 잡기 전에 해당 반송 레이블이 적합한 디바이스에 부착되었는지 확인하십시오.
     {: note}
2. 인벤토리 목록을 사용하여 모든 케이블과 광학장치가 반환되어 운송용 케이스에 보관되었는지 확인하십시오. 
3. 인벤토리 목록을 운송용 케이스에 다시 넣은 후 반송 레이블에 나열된 지시사항에 따라 디바이스에 레이블을 부착하십시오. 
4. 운송 업체와 픽업 스케줄을 잡은 후 디바이스를 데이터 센터로 반환하십시오. 

    디바이스가 {{site.data.keyword.cloud_notm}}로 반환되면 {{site.data.keyword.mdms_short}} 요청 세부사항 페이지에서 주문 상태가 _디바이스를 수령함_으로 변경됩니다. 

## 다음 단계
{: #return-device-next-steps}

- [{{site.data.keyword.mdms_short}} 요청을 관리](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request)하여 주문 상태를 확인하십시오. 
- 소스 서버에서 데이터를 삭제하기 전에 [데이터가 {{site.data.keyword.cloud_notm}}에 성공적으로 업로드되었는지 확인](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data)하십시오. 

