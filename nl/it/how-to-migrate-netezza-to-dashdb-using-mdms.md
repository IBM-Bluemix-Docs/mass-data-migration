---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Migrazione dei database Netezza a DashDB

Il servizio Mass Data Migration Service (MDMS) consente di migrare database Netezza di grandi dimensioni in DashDB.

Questo documento descrive:
- gli strumenti Netezza per determinare la quantità di dati da trasferire tramite il servizio Mass Data Migration Service,
- i comandi per esportare i dati nel dispositivo Mass Data Migration.

## Dimensionamento del database
1. Da [IBM Support: Fix Central - Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window} scarica la versione appropriata degli strumenti Netezza che corrisponde alla tua istanza Netezza.

   **NOTA** - Per impostazione predefinita, gli strumenti di supporto sono installati sul server Netezza nella directory /nz/support-IBM_Netezza<version>/bin
   
2. i seguenti due comandi: `nz_db_size` e `nz_compressedTableRatio`

  ```
  nz_db_size
Oggetto | Nome | Byte | KB | MB | GB | TB
-----------------------------------------------------------------------------------------------------------
Dispositivo | cdcntze1 | 23,388,712,337,408 | 22,840,539,392 | 22,305,214 | 21,782.4 | 21.3
Database | DHDB | 183,537,500,160 | 179,235,840 | 175,035 | 170.9 | .2
Tabella | DH71964I1 | 880,803,840 | 860,160 | 840 | .8 | .0
Tabella | DH71964T1 | 96,120,078,336 | 93,867,264 | 91,667 | 89.5 | .1
Tabella | DH71964T10 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T2 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T3 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T4 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T5 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T6 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T7 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T8 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabella | DH71964T9 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
  ```
  
  
  ```
  nz_compressedTableRatio
  ....................................................................................
  . I seguenti valori mostrano il rapporto di dimensioni stimato di una tabella compressa nella sua .
  . forma non compressa. Una tabella non compressa è approssimativamente <ratio> volte più grande .
  . della sua versione compressa. .
  . .
  . La 'Dimensione compressa' è la quantità effettiva di archiviazione utilizzata dalla tabella. .
  . La 'Dimensione non compressa' è una stima basata su calcoli matematici. .
  ....................................................................................
  Database: DHDB
Nome tabella/MView Rapporto Dimensione compressa Dimensione non compressa Differenza dimensioni
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
Totale per questo database 1.50 183,537,500,160 275,251,242,240 91,713,742,080
  ```

## Estrazione dati e procedura di incorporamento

Per estrarre i dati da Netezza sono disponibili due opzioni:
1. Utilizzare il **programma di utilità nz_backup**:

  ```
  /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
  ```
   
   **NOTA**: tieni presente che {target_directory} è la condivisione NFS fornita dal dispositivo MDMS, montata su questo server.
   
2. Utilizzare CREATE EXTERNAL TABLE
   - Fornisci al team DashDB la clausola “USING” utilizzata per l'esportazione per il riutilizzo durante il processo LOAD
   - Seleziona FORMAT = ”Text”
   
   
## Convalida dei dati
I dati possono essere riletti su Netezza usando la selezione dalla tabella esterna **myfile** `USING(....) “` per garantire che i dati siano corretti.
 
## Ulteriori informazioni
Ulteriori informazioni su Netezza sono disponibili nella [documentazione utente del database IBM Netezza](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
