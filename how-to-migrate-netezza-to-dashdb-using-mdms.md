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

# Migrating Netezza databases to DashDB

The Mass Data Migration Service (MDMS) can be used to migrate large Netezza databases to DashDB. You can use this document as a reference for the tools that determine the amount of data to be transferred, and exporting methods.

## Determining the database object size
1. From [IBM Support > Fix Central > Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}, download the appropriate Netezza Tools version that corresponds to your Netezza instance.

   By default, support tools are installed on Netezza server at directory `/nz/support-IBM_Netezza<version>/bin`
   {:note}

2. Run the following two commands.
   - `nz_db_size` to determine the size of the database

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

   - `nz_compressedTableRatio` to estimate the size of the data when it is decompressed.

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

## Extracting data and onboarding

You can use two options to extract the data from Netezza.
- Use the `nz_backup` utility.
   ```
   /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
   ```

   The `{target_directory}` is the NFS share that is provided by the MDMS device, and mounted to this server.
   {:tip}

- Use the `CREATE EXTERNAL TABLE` statement.
   - Select `FORMAT` = ”Text”
   - Provide the DashDB team the `USING` clause that was used for export for reuse during the `LOAD` process.


## Validating data
The data can be reread back on the Netezza by using the `SELECT FROM` statement with the external table `myfile` and a `USING(....)` clause to ensure that the data is correct.

**Additional information**

More information about Netezza, see [IBM Netezza database user documentation](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
