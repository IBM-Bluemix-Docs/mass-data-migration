---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-31"

---
{:codeblock: .codeblock}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# 將 Netezza 資料庫移轉至 DashDB

Mass Data Migration Service (MDMS) 可用來將大型 Netezza 資料庫移轉至 DashDB。您可以使用本文件作為工具的參照，而這些工具決定要傳送的資料量及匯出方法。

## 決定資料庫物件大小
1. 從 [IBM 支援中心 > 修正程式中心 > Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}，下載與您的 Netezza 實例相對應的適當 Netezza Tools 版本。

   依預設，支援工具會安裝在 Netezza 伺服器的 `/nz/support-IBM_Netezza<version>/bin` 目錄中
   {:note}

2. 執行下列兩個指令。
   - `nz_db_size` 以決定資料庫大小

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

   - `nz_compressedTableRatio` 估計資料解壓縮時的大小。

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

## 擷取資料及上線

您可以使用兩個選項，從 Netezza 擷取資料。
- 使用 `nz_backup` 公用程式。
   ```
  /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
  ```

   `{target_directory}` 是 MDMS 裝置所提供的 NFS 共用，並裝載至此伺服器。
   {:tip}

- 使用 `CREATE EXTERNAL TABLE` 陳述式。
   - 選取 `FORMAT` = ”Text”
   - 向 DashDB 團隊提供在 `LOAD` 處理程序期間用於匯出以供重複使用的 `USING` 子句。


## 驗證資料
搭配使用 `SELECT FROM` 陳述式與外部表格 `myfile` 及 `USING(....)` 子句，以在 Netezza 上重新讀取資料，確保資料正確。

**其他資訊**

[IBM Netezza 資料庫使用者文件](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}中會提供其他 Netezza 相關資訊。
