---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: migrate Netezza databases, PureData System for Analytics databases, 

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

# PureData System for Analytics 데이터베이스를 {{site.data.keyword.dashdbshort_notm}}로 마이그레이션
{: #migrate-netezza-databases}

{{site.data.keyword.mdms_full}}은 대형 IBM PureData™ System for Analytics(Netezza® 기술로 구동됨) 데이터베이스를 {{site.data.keyword.dashdbshort}}로 마이그레이션하는 데 사용할 수 있습니다. 이 문서를 전송할 데이터의 양을 판별하는 도구 및 내보내기 방법에 대한 참조로 사용할 수 있습니다.
{: shortdesc}

## 데이터베이스 오브젝트 크기 판별
{: #determine-db-object-size}

1. [IBM 지원 센터 > Fix Central > Netezza 도구 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}에서 Netezza 인스턴스에 해당하는 적합한 Netezza 도구 버전을 다운로드하십시오.

   기본적으로 지원 도구는 Netezza 서버에서 `/nz/support-IBM_Netezza<version>/bin` 디렉토리에 설치됩니다.
   {:note}

2. 다음 두 가지 명령을 실행하십시오.
   - 데이터베이스 크기를 판별하기 위한 `nz_db_size`

     ```
     nz_db_size
     Object | Name | Bytes | KB | MB | GB | TB
     -----------------------------------------------------------------------------------------------------------
     Appliance | cdcntze1 | 23,388,712,337,408 | 22,840,539,392 | 22,305,214 | 21,782.4 | 21.3
     Database | DHDB | 183,537,500,160 | 179,235,840 | 175,035 | 170.9 | .2
     Table | DH71964I1 | 880,803,840 | 860,160 | 840 | .8 | .0
     Table | DH71964T1 | 96,120,078,336 | 93,867,264 | 91,667 | 89.5 | .1
     Table | DH71964T10 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T2 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T3 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T4 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T5 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T6 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T7 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T8 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     Table | DH71964T9 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
     ```
     {: codeblock}

   - 압축을 풀었을 때의 데이터 크기를 예상하기 위한 `nz_compressedTableRatio`

      ```
      nz_compressedTableRatio
      ....................................................................................
      . The values below show the estimated size ratio of a compressed table to its .
      . uncompressed form. An uncompressed table is approximately <ratio> times larger .
      . than its compressed version. .
      . .
      . The 'Compressed Size' is the actual amount of storage being used by the table. .
      . The 'Uncompressed Size' is an estimate based on mathematical calculations. .
      ....................................................................................
      Database: DHDB
      Table/MView Name Ratio Compressed Size Uncompressed Size Size Difference
      ================== ===== ================ =============== ===========
      DH71964I1 1.49 880,803,840 1,310,723,840 429,920,000
      DH71964T1 1.50 96,120,078,336 144,179,203,840 48,059,125,504
      DH71964T10 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T2 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T3 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T4 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T5 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T6 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T7 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T8 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      DH71964T9 1.50 9,615,179,776 14,417,923,840 4,802,744,064
      ================================ ===== =================== ===================
      Total For This Database 1.50 183,537,500,160 275,251,242,240 91,713,742,080
      ```
      {: codeblock}

## 데이터 추출 및 온보딩
{: #extract-data}

두 가지 옵션을 사용하여 Netezza에서 데이터를 추출할 수 있습니다.
- `nz_backup` 유틸리티를 사용하십시오.
   ```
   /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
   ```

   `{target_directory}`는 MDMS 디바이스에서 제공하는 NFS 공유이며 이 서버에 마운트됩니다.
   {:tip}

- `CREATE EXTERNAL TABLE` 문을 사용하십시오.
   - `FORMAT` = ”Text”를 선택하십시오.
   - `LOAD` 프로세스 중에 재사용을 위해 내보내는 데 사용된 `USING` 절을 {{site.data.keyword.dashdbshort_notm}} 팀에 제공하십시오. 


## 데이터 유효성 검증
{: #validate-data}

데이터가 올바른지 확인하기 위해 외부 테이블이 `myfile`인 `SELECT FROM` 문과 `USING(....)` 절을 사용하여 Netezza에서 데이터를 다시 읽을 수 있습니다.

**추가 정보**

PureData System for Analytics에 대한 자세한 정보는 [IBM Netezza 데이터베이스 사용자 문서![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}를 참조하십시오. 
