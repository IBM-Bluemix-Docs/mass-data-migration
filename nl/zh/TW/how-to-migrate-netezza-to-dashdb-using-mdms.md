---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# 將 Netezza 資料庫移轉至 DashDB

Mass Data Migration Service (MDMS) 可用來將大型 Netezza 資料庫移轉至 DashDB。

本文件說明：
- Netezza 工具，用來判斷要透過 Mass Data Migration Service 傳送的資料量。
- 各項指令，用來將資料匯出至 Mass Data Migration 裝置。

## 資料庫大小
1. 從[IBM 支援中心：修正程式中心 - Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}，下載與您的 Netezza 實例相對應的適當 Netezza Tools 版本。

   **附註** - 依預設，支援工具會安裝在 Netezza 伺服器的 /nz/support-IBM_Netezza<version>/bin 目錄中
   
2. 下列兩個指令：`nz_db_size` 及 `nz_compressedTableRatio`

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

## 資料擷取及上線程序

您可以利用下列兩個選項從 Netezza 中擷取資料：
1. 使用 **nz_backup 公用程式**：

  ```
  /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
  ```
   
   **附註**：請注意，{target_directory} 是 MDMS 裝置所提供的 NFS 共用，已裝載至此伺服器。
   
2. 使用 CREATE EXTERNAL TABLE
   - 向 DashDB 團隊提供在載入過程中用於匯出以供重複使用的 "USING" 子句
   - 選取 FORMAT = ”Text”
   
   
## 資料驗證
使用從外部表格 **myfile** `USING(....) ` 中的選擇，在 Netezza 上重新讀取資料，以確定資料正確無誤。
 
## 其他資訊
[IBM Netezza 資料庫使用者文件](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}中會提供其他 Netezza 相關資訊。
