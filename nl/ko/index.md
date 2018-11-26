---

copyright:
  years: 2017-2018
lastupdated: "2018-10-31"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# {{site.data.keyword.cloud_notm}} 대량 데이터 마이그레이션 시작하기

**전제조건**

대량 데이터 마이그레이션 요청을 제출하고 마이그레이션을 완료하기 전에 다음 정보를 수집하십시오. 

1. 스토리지 디바이스의 네트워크 설정
   - 정적 IP 주소
   - 데이터 전송을 사용하기 위한 넷마스크
2. 원격 컴퓨터에 대한 네트워크 설정
   - 정적 IP 주소
   - 넷마스크
   - 사용자 인터페이스에 액세스하기 위한 기본 게이트웨이
3. Cloud Object Storage 다운로드 대상 <br/>
   
   요청 양식을 완료하려면 US Standard Cross Region 또는 EU Cross Region 위치에 하나의 버킷과 하나 이상의 {{site.data.keyword.cos_full}} 계정이 있어야 합니다. 아직 {{site.data.keyword.cos_full_notm}}} 계정이 없으면 대량 데이터 마이그레이션 디바이스를 요청하기 전에 계정을 작성하십시오. [{{site.data.keyword.cos_full}} 정보](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}를 참조하십시오.
   {:important}

## 요청 작성

1. 고유 인증 정보를 사용하여 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}에 로그인하십시오.
2. 탐색줄에서 **스토리지** > **데이터 마이그레이션** > **대량 데이터 마이그레이션**을 선택하여 대량 데이터 마이그레이션 시작 페이지에 액세스하십시오.
3. **디바이스 요청**을 클릭하여 주문 양식을 여십시오.
4. **대량 데이터 마이그레이션** 주문 양식의 각 필드를 기입하십시오.
   - **발송 주소** - 이 양식은 미리 채워져 있지 않으며 각 필드는 편집 가능합니다. 주의 필드에 디바이스 전달을 수락할 사람의 이름을 제공하십시오. 전달 위치를 선택할 때 디바이스의 중량(케이스 포함 66lb.) 및 접근성을 고려하십시오.
   
   디바이스에는 손쉬운 조작을 위한 휠과 팝업 핸들이 장착되어 있습니다.
   {:note}

   - **주요 마이그레이션 연락처** - 이 양식은 미리 채워져 있지 않습니다. 각 필드는 편집 가능합니다. 두 명 이상을 추가할 수 있습니다.
   - **데이터 센터 네트워크 구성** - 발송 전에 대량 데이터 마이그레이션 디바이스에서 Eth3 포트의 사전 프로비저닝을 위한 네트워크 구성 세부사항을 제공하십시오.
   - **데이터 오프로드 대상** 목록에서 기존 대상 계정을 선택하십시오.
   - **요청 이름** - 주문을 추적하는 데 도움이 되는 이름을 입력하십시오.
5. 각 서비스 계약을 읽은 후 **대량 데이터 마이그레이션 계약의 전체 이용 약관을 읽고 이에 동의합니다.** 선택란을 선택하십시오.
6. **요청 제출**을 클릭하여 요청을 제출하십시오. 양식을 완전히 포기하고 대량 데이터 마이그레이션 시작 페이지로 돌아가려면 **취소**를 클릭하십시오.


## 준비 및 발송

요청을 제출한 후 요청 티켓의 상태는 `Processing Request`로 표시됩니다. 요청이 허용되면 {{site.data.keyword.IBM}}에서는 사용 가능한 다음 디바이스를 사전 구성하기 시작합니다.

디바이스를 준비하는 중이면 [요청](https://control.softlayer.com/storage/mdms){:new_window} 페이지의 상태가 차례로 `Prepping Device` 및 `Awaiting Shipment`로 표시됩니다. 요청이 `Awaiting Shipment` 상태가 된 후에는 더 이상 이를 취소할 수 없습니다.

운송 업체가 사용자 위치로 발송하기 위해 디바이스를 픽업하면 요청 상태는 `Device Shipped`로 업데이트됩니다. 추적 번호는 [요청](https://control.softlayer.com/storage/mdms){:new_window} 페이지의 **주문 세부사항** 섹션에서 공유됩니다.


## 수신 및 연결

1. 디바이스는 사전 구성된 상태로 도착합니다. 기본 [전원 공급 및 연결 지시사항](user-instructions.html)이 포함되어 있습니다. <br/>
  
   사용자 이름 및 스토리지 풀 비밀번호는 별도로 제공됩니다. 인증 정보에 대해서는 [요청](https://control.softlayer.com/storage/mdms){:new_window}의 **요청 세부사항**을 확인하십시오.
   {:note}
2. 브라우저에서 주문 양식에 제공한 정적 IP 주소로 이동하십시오.
3. 로그인하고 비밀번호를 입력하여 빈 스토리지 풀을 잠금 해제하십시오. <br/>
   
   비밀번호에 대해서는 [요청](https://control.softlayer.com/storage/mdms){:new_window} 페이지의 요청 세부사항을 참조하십시오.
   {:tip}
4. 서버에 NFS 공유를 마운트하십시오.
5. DataShuttle 인벤토리를 다시 실행하여 새 파일이 캡처되었는지 확인하십시오.

## 데이터 이동
1. DataShuttle 복사를 실행하여 데이터를 이동하십시오.
2. 스토리지 풀을 잠그십시오.
3. 대량 데이터 마이그레이션 디바이스를 정상 종료하십시오.
4. 제공된 발송 레이블을 사용하여 상자를 {{site.data.keyword.BluSoftlayer_full}} 데이터 센터로 반송하십시오.

디바이스가 {{site.data.keyword.BluSoftlayer}}에 환반되면 요청 상태는 `Device Received`로 변경됩니다.

## 오프로드 및 액세스

전송 프로세스 중에 요청 상태는 `Offloading Data`로 표시됩니다. {{site.data.keyword.objectstorageshort}} 버킷으로 마이그레이션이 완료되면 상태가 다시 변경됩니다(`Offload Complete`). Cloud Object Storage 버킷으로 고속 오프로드가 완료되면 데이터에 즉시 액세스할 수 있습니다.

## 디바이스 지우기

{{site.data.keyword.IBM}}에서는 디바이스의 데이터를 영구적으로 지우기 위해 DOD 레벨 데이터 지우기 요구사항을 구현합니다. 완료되면 요청 상태는 `Erase Complete`로 표시됩니다.
