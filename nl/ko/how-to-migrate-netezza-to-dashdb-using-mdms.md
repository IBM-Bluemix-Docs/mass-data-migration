---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# DashDB로 Netezza 데이터베이스 마이그레이션

대량 데이터 마이그레이션 서비스(MDMS)는 대형 Netezza 데이터베이스를 DashDB로 마이그레이션하는 데 사용할 수 있습니다.

이 문서에서는 다음에 대해 설명합니다.
- 대량 데이터 마이그레이션 서비스를 통해 전송할 데이터 크기를 판별하는 Netezza 도구.
- 대량 데이터 마이그레이션 디바이스로 데이터를 내보내는 명령.

## 데이터베이스 크기 조정
1. [IBM Support: Fix Central - Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}에서 Netezza 인스턴스에 대응하는 적절한 Netezza Tools 버전을 다운로드하십시오.

   **참고** - 기본적으로 지원 도구는 Netezza 서버 /nz/support-IBM_Netezza<version>/bin 디렉토리에 설치됩니다.

2. 다음 두 명령이 사용됩니다. `nz_db_size` 및 `nz_compressedTableRatio`

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

## 데이터 추출 및 온보딩 프로시저

Netezza에서 데이터를 추출하는 데 사용할 수 있는 두 가지 옵션이 있습니다.
1. **nz_backup 유틸리티** 사용:

  ```
  /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
  ```

   **참고**: {target_directory}는 이 서버에 마운트된 MDMS 디바이스가 제공하는 NFS 공유입니다.

2. CREATE EXTERNAL TABLE 사용:
   - LOAD 프로세스 중 재사용을 위해 내보내는 데 사용된 “USING” 절을 DashDB 팀에 제공
   - FORMAT = ”Text” 선택


## 데이터 유효성 검증
“select from 외부 테이블 **myfile** `USING(....) “`을 사용하여 Netezza에서 데이터를 다시 읽어서 데이터가 올바른지 확인할 수 있습니다.

## 추가 정보
Netezza에 대한 자세한 정보는 [IBM Netezza database user documentation](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}에 있습니다.
