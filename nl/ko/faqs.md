---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# FAQ
{: #faqs}

{{site.data.keyword.mdms_full}}에 대해 자주 질문되는 내용(FAQ)입니다.
{: shortdesc}

## {{site.data.keyword.mdms_full_notm}}이란 무엇입니까? 
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}}은 120TB 용량의 튼튼한 휴대용 스토리지 디바이스를 이용하여 테라바이트에서 페타바이트에 이르는 데이터를 {{site.data.keyword.cloud_notm}}로 안전하게 이동하는 작업을 신속하게 처리하는 물리적 데이터 전송 서비스입니다. 

## {{site.data.keyword.mdms_short}} 사용을 시작하는 방법은 무엇입니까? 
{: #how-to-use-mdms}
{: faq}

[{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}을 사용하여 요청을 제출하십시오. 일단 요청이 승인되고 처리되면 사용 가능한 다음 디바이스가 구성되어 네트워크 및 발송 정보에 기반하여 사용자에게 발송됩니다. 

## {{site.data.keyword.mdms_short}}은 누가 사용해야 합니까? 
{: #who-uses-mdms}
{: faq}

데이터 센터 및 사무실에서 석유 굴착 장치 및 선박과 같은 원격 위치에 이르기까지, {{site.data.keyword.mdms_short}} 디바이스는 거의 모든 환경에서 작동할 수 있습니다. {{site.data.keyword.mdms_short}}은 또한 네트워크상 데이터 전송 옵션이 너무 비싸거나 속도가 너무 느리거나 사용 불가능한 경우 훌륭한 대안이 되기도 합니다. 

## {{site.data.keyword.mdms_short}}을 사용하여 얼마나 많은 데이터를 전송할 수 있습니까? 
{: #how-much-data}
{: faq}

전송할 수 있는 데이터의 양에는 테라바이트에서 페타바이트에 이르기까지 사실상 제한이 없습니다. 각 디바이스는 RAID-6에서 최대 120TB 가용 용량을 보유하지만 더 큰 워크로드를 수용하기 위해 여러 디바이스를 사용할 수 있습니다. {{site.data.keyword.mdms_short}}은 또한 인라인 압축도 제공하므로, 데이터 세트를 얼마나 압축할 수 있는지에 따라 사용 가능한 용량이 더 늘어날 수도 있습니다. 가장 큰 단일 오브젝트는 크기가 10 TB로 제한됩니다. 


## 여러 디바이스를 사용하여 120TB를 초과하는 대형 워크로드를 이동하려면 어떻게 해야 합니까? 
{: #using-multiple-devices}
{: faq}

여러 디바이스를 병렬 또는 직렬로 사용하여 한 번의 마이그레이션으로 모든 데이터를 이동하거나 하나의 디바이스를 사용하여 마이그레이션을 반복 수행하십시오. 예를 들어, 9개 디바이스를 병렬로 사용하여 1PB의 데이터를 전송하거나 1개의 디바이스를 사용하여 개별 마이그레이션을 9회 수행합니다. 여러 디바이스를 병렬로 사용할 경우에는 수집 속도가 느려진다는 점을 유념하십시오. 

## 데이터를 전송하는 데 얼마나 걸립니까? 
{: #transfer-timeline}
{: faq}

고객이 {{site.data.keyword.mdms_short}} 요청을 제출한 시간부터 IBM Cloud Object Storage 버킷에서 고객 데이터에 액세스할 수 있게 될 때까지의 총 처리 시간은 며칠이 걸릴 수 있습니다. 전송 성능은 네트워킹, 대역폭 또는 전송 중인 파일의 수와 같은 여러 요인의 영향을 받을 수 있습니다. 예를 들어 동일한 양의 데이터를 수백만 개의 작은 파일로 전송할 경우 상대적으로 더 적은 수의 큰 파일로 전송할 때보다 시간이 오래 걸립니다. 

## {{site.data.keyword.mdms_short}} 디바이스를 얼마나 오래 보유할 수 있습니까? 
{: #device-onsite-time}
{: faq}

영업일 기준 첫 10일 동안은 추가 비용 없이 디바이스를 현장에서 보유할 수 있습니다. 이 기간에는 디바이스가 배송된 날과 디바이스를 IBM으로 반환한 날(최대 2일)은 포함되지 않습니다. 수집을 완료하는 데 시간이 더 필요하면 그 이후에 1일당 30달러를 지불하고 사용 기간을 연장할 수 있습니다. 이 사항은 모든 지역에 적용됩니다. 

## {{site.data.keyword.mdms_short}}에서는 어떤 네트워크 인터페이스를 지원합니까? 
{: #supported-network-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} 디바이스는 RJ45(CAT6a) 및 SFP+ 구리선 네트워크 포트를 포함한 10Gbps 네트워크 인터페이스를 제공합니다. 

RJ45 - SFP+ 변환기는 SFP+ 기본 연결이 없는 디바이스 모델에만 포함되어 있습니다. 이때 광섬유는 지원되지 않습니다. 

## {{site.data.keyword.mdms_short}} 기본 배송 옵션은 무엇입니까? 
{: #shipping-options}
{: faq}

{{site.data.keyword.mdms_short}}은 모든 디바이스를 배송하는 데 UPS Next Day Air 왕복 배송을 사용합니다. 비용은 디바이스당 USD 395의 저렴한 고정 요금에 포함됩니다. 현재는 고객이 다른 발송 방법을 선택할 수 없습니다.


## 어떤 지역에서 {{site.data.keyword.mdms_short}}을 사용할 수 있습니까? 
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}}은 현재 미국(US), 유럽 연합(EU), 일본, 오스트레일리아, 브라질, 싱가포르, 홍콩, 노르웨이, 한국, 캐나다, 멕시코에서 사용할 수 있습니다. 사용 가능한 지역을 더 확장하고 있는 중입니다. 온라인 주문은 대부분의 지역에서 가능합니다. 온라인 주문이 불가능한 지역의 경우 IBM 영업 담당자를 통해 서비스 사용에 대해 문의하십시오. 

국경을 벗어나서 디바이스를 배송할 수는 없습니다. 즉, 한 지역에서 주문하고 다른 지역으로 배송할 수 없습니다. 단, EU 및 28개 소속 국가의 경우는 예외입니다.
{: note}

## 미국의 {{site.data.keyword.mdms_short}} 기본 배송 옵션은 무엇입니까? 
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}}은 미국 디바이스에 대해 왕복 UPS 야간 배송을 사용합니다. 배송비는 가격에 포함되어 있습니다. 현재는 고객이 다른 배송 방법을 선택할 수 없습니다.  

## EU의 {{site.data.keyword.mdms_short}} 기본 배송 옵션은 무엇입니까? 
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}}은 EU 디바이스에 대해 왕복 FedEx 야간 배송을 사용합니다. 배송비는 가격에 포함되어 있습니다. 현재는 고객이 다른 배송 방법을 선택할 수 없습니다.  

## 기타 지원되는 모든 지역의 {{site.data.keyword.mdms_short}} 기본 배송 옵션은 무엇입니까? 
{: #default-shipping-other}
{: faq}

미국 및 EU를 제외한 지원되는 모든 지역의 경우, 배송 업체 및 배송 처리 시간이 다릅니다. 배송비는 가격에 포함되어 있습니다. 현재는 고객이 다른 배송 방법을 선택할 수 없습니다. 

이러한 지역에서 IBM은 주문이 접수될 때 왕복 배송을 예약할 수 없습니다. 대신, 배송이 필요할 때 편도 배송이 예약됩니다. 아웃바운드 배송의 경우 요청을 제출한 후 IBM에서 {{site.data.keyword.mdms_short}} 디바이스의 배송을 조정할 수 있도록 최소 3일(영업일 기준)을 허용하십시오.
{: note}

미국 및 EU 이외 지역 주문의 경우, 원하는 디바이스 배송 날짜보다 최소 3일(영업일) 전에 디바이스에 대한 반송을 요청하십시오. 예를 들어 디바이스를 금요일에 배송하고 싶은 경우, 반송을 같은 주의 월요일로 조정하십시오. 반송은 {{site.data.keyword.mdms_short}} 대시보드의 _요청 세부사항_ 탭에서 요청할 수 있습니다.
{: important}

## 거주 지역이 일본, 오스트레일리아, 브라질, 캐나다, 멕시코, 홍콩, 싱가포르, 노르웨이 또는 한국입니다. {{site.data.keyword.mdms_short}} 디바이스의 반송을 요청하는 방법은 무엇입니까? 
{: #shipping-timetable-other}
{: faq}

미국 및 EU 이외 지역에서 {{site.data.keyword.mdms_short}}을 사용 중인 경우 원하는 디바이스 배송 날짜보다 최소 3일(영업일) 전에 디바이스에 대한 반송을 요청해야 합니다. 예를 들어 디바이스를 금요일에 배송하고 싶은 경우, 반송을 같은 주의 월요일로 조정하십시오. 

## 데이터를 {{site.data.keyword.cloud_notm}}로 가져오는 데 어느 정도의 비용이 듭니까? 
{: #data-transfer-cost}
{: faq}

데이터를 {{site.data.keyword.cloud_notm}}로 전송할 때 비용이 발생하지 않습니다. 


## {{site.data.keyword.mdms_short}}을 사용하여 {{site.data.keyword.cloud_notm}} 외부로 데이터를 내보낼 할 수 있습니까? 
{: #exporting-data}
{: faq}

{{site.data.keyword.mdms_short}}은 현재 {{site.data.keyword.cloud_notm}} 외부로 데이터 내보내기를 지원하지 않습니다. 


## {{site.data.keyword.mdms_short}}은 데이터를 암호화합니까? 
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}}은 AES 256비트 암호화로 모든 데이터를 암호화하고 스토리지 풀을 잠금 해제하기 위한 강력한 비밀번호를 제공합니다. {{site.data.keyword.IBM}} 내 모든 데이터 전송은 SSL을 통해 수행됩니다.

## {{site.data.keyword.mdms_short}}은 실제로 어떻게 데이터를 보호합니까? 
{: #security}
{: faq}

모든 {{site.data.keyword.mdms_short}} 디바이스는 튼튼하고 내구성이 강한 격납장치에 들어 있습니다. 이 케이스는 방수, 충격 방지, 조작 방지 기능이 있어서 디바이스 왕복 및 데이터 보안을 보장합니다.

## 마이그레이션 프로세스 전체에서 내 요청을 어떻게 추적할 수 있습니까? 
{: #how-to-track-request}
{: faq}

요청 상태를 추적하려면 {{site.data.keyword.cloud_notm}} 콘솔의 {{site.data.keyword.mdms_short}} 대시보드에 있는 _요청 세부사항_ 탭으로 이동하십시오. 

## 데이터가 {{site.data.keyword.cos_full_notm}}로 오프로드된 이후 {{site.data.keyword.mdms_short}} 디바이스에서
어떻게 데이터를 지웁니까? 
{: #data-erasure}
{: faq}

IBM Cloud Object Storage로 데이터 오프로드가 완료되는 즉시 IBM에서는 모든 고객 데이터가 디바이스에서 완전하게 지워지도록 NIST 데이터 지우기 표준을 사용하여 디바이스를 즉시 지웁니다. 

## {{site.data.keyword.mdms_short}}에서 파일 인터페이스는 무엇입니까? 
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}}은 NFS(Network File System) 및 SMB(Server Message Block) 프로토콜을 지원합니다. 

## {{site.data.keyword.mdms_short}}에서 파일 인터페이스는 어떻게 사용합니까? 
{: #how-to-use-file-interface}
{: faq}

먼저 암호화 풀을 잠금 해제하십시오. 그런 다음 마이그레이션하려는 데이터를 포함하는 서버에 공유를 마운트하십시오. 네트워크 공유로 데이터 파일 복사를 시작하십시오. 

## {{site.data.keyword.mdms_short}}에서 파일 인터페이스의 이점은 무엇입니까? 
{: #file-interface-benefits}
{: faq}

파일 인터페이스는 많은 대용량 파일을 {{site.data.keyword.cloud_notm}}에 복사 및 전송할 수 있도록 하는 다양한 기능의 파일 및 네트워크 소프트웨어에 기반합니다.

## {{site.data.keyword.mdms_short}} 디바이스에서 파일은 어떻게 저장됩니까? 
{: #file-storage}
{: faq}

{{site.data.keyword.mdms_short}} 디바이스는 LZ4 압축 및 AES 256비트 암호화를 활용하는 ZFS 파일 시스템을 사용합니다. 

## 미국에서 {{site.data.keyword.mdms_short}}을 사용하는 데 어느 정도의 비용이 듭니까? 
{: #pricing-us}
{: faq}

미국의 경우, 디바이스 사용료 295달러, 왕복 UPS 야간 배송료 100달러 및 영업일 기준 10일간의 현장 사용을 포함하여 디바이스당 395달러의 고정 요금이 부과됩니다. 

10일간의 현장 사용에는 디바이스가 배송된 날과 디바이스를 IBM으로 반환한 날(최대 2일)은 포함되지 않습니다. 마이그레이션을 완료하는 데 할당된 10일 이상의 시간이 필요할 경우 추가 일 수에 대해 1일당 30달러의 연장 수수료가 부과됩니다. 

## EU에서 {{site.data.keyword.mdms_short}}을 사용하는 데 어느 정도의 비용이 듭니까? 
{: #pricing-eu}
{: faq}

EU의 경우, 디바이스 사용료 295달러, 왕복 FedEx 야간 배송료 150달러 및 영업일 기준 10일간의 현장 사용을 포함하여 디바이스당 445달러의 고정 요금이 부과됩니다. 

10일간의 현장 사용에는 디바이스가 배송된 날과 디바이스를 IBM으로 반환한 날(최대 2일)은 포함되지 않습니다. 마이그레이션을 완료하는 데 할당된 10일 이상의 시간이 필요할 경우 추가 일 수에 대해 1일당 30달러의 연장 수수료가 부과됩니다. 

## 기타 지원되는 모든 지역에서 {{site.data.keyword.mdms_short}}을 사용하는 데 어느 정도의 비용이 듭니까? 
{: #pricing-other}
{: faq}

기타 모든 지역(일본, 오스트레일리아, 브라질, 캐나다, 멕시코, 홍콩, 싱가포르, 노르웨이, 한국)의 경우, 디바이스 사용료 295달러, 왕복 배송료 850달러 및 영업일 기준 10일간의 현장 사용을 포함하여 디바이스당 1,145달러의 고정 요금이 부과됩니다. 

10일간의 현장 사용에는 디바이스가 배송된 날과 디바이스를 IBM으로 반환한 날(최대 2일)은 포함되지 않습니다. 마이그레이션을 완료하는 데 할당된 10일 이상의 시간이 필요할 경우 추가 일 수에 대해 1일당 30달러의 연장 수수료가 부과됩니다. 

해당 지역의 경우 특별한 배송 요구사항이 있습니다. 자세한 정보는 위 내용을 참조하십시오.
{: note}

## {{site.data.keyword.cos_full_notm}} 사용에 대해 요금이 부과됩니까? 
{: #pricing-cos}
{: faq}

데이터를 {{site.data.keyword.cloud_notm}}로 전송하는 것은 무료입니다. 하지만 {{site.data.keyword.cos_full_notm}} 또는 다른 모든 {{site.data.keyword.cloud_notm}} 서비스에 저장된 데이터에는 표준 요금이 적용됩니다. Cloud Object storage의 가격 옵션에 대한 자세한 정보는 [{{site.data.keyword.cos_full_notm}} 가격](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}을 참조하십시오.  

## {{site.data.keyword.mdms_full_notm}} 디바이스를 구입할 수 있습니까? 
{: #purchasing-devices}
{: faq}

{{site.data.keyword.mdms_full_notm}} 디바이스는 구입할 수 없습니다. 

## {{site.data.keyword.mdms_short}} 프로세스가 고유한 오브젝트 이름을 유지하는 방법은 무엇입니까? 
{: #object-name-uniqueness}
{: faq}

오브젝트 이름이 Cloud Object Storage 버킷으로 복사될 때 고유성을 보장하기 위해 오브젝트 이름의 접두부에 파일 경로가 포함됩니다. 예를 들어, 버킷으로 복사될 때 `/root/user/config.ini`는 `root/user/config.ini`가 됩니다. 

## {{site.data.keyword.cos_full_notm}} 계정에 대상 버킷이 존재하지 않으면 어떻게 됩니까? 
{: #target-buckets}
{: faq}

대상 버킷이 존재하지 않으면 버킷이 작성됩니다. 존재하는 경우에 버킷은 비어 있어야 합니다. 그렇지 않으면 복사를 진행할 수 없습니다.  

## 스캔 프로세스 중에는 링크를 건너뜁니까?
{: #links-scan-process}
{: faq}

예. 스캔 프로세스 중에는 Symlink 및 하드 링크를 건너뜁니다.
