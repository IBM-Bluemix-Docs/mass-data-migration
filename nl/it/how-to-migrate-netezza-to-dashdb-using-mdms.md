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

# Migrazione dei database Netezza a DashDB

Il servizio Mass Data Migration Service (MDMS) consente di migrare database Netezza di grandi dimensioni in DashDB. Puoi utilizzare questo documento come riferimento per gli strumenti che determinano la quantità di dati da trasferire e i metodi di esportazione.

## Determinazione della dimensione dell'oggetto del database
1. Da [IBM Support > Fix Central > Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}, scarica la versione appropriata degli strumenti Netezza che corrisponde alla tua istanza Netezza.

   Per impostazione predefinita, gli strumenti di supporto sono installati sul server Netezza nella directory `/nz/support-IBM_Netezza<version>/bin`
   {:note}

2. Immetti i seguenti due comandi.
   - `nz_db_size` per determinare la dimensione del database

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

   - `nz_compressedTableRatio` per stimare la dimensione dei dati dopo la decompressione.

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
      {: codeblock}

## Estrazione dei dati e onboarding

Puoi utilizzare due opzioni per estrarre i dati da Netezza.
- Utilizza il programma di utilità `nz_backup`.
   ```
   /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
   ```

   `{target_directory}` è la condivisione NFS fornita dal dispositivo MDMS e montata su questo server.
   {:tip}

- Utilizza l'istruzione `CREATE EXTERNAL TABLE`.
   - Seleziona `FORMAT` = ”Text”
   - Fornisci al team DashDB la clausola `USING` utilizzata per l'esportazione per il riutilizzo durante il processo `LOAD`.


## Convalida dei dati
I dati possono essere riletti su Netezza usando l'istruzione `SELECT FROM` con la tabella esterna `myfile` e una clausola `USING(....)` per assicurarti che i dati siano corretti.

**Informazioni aggiuntive**

Per ulteriori informazioni su Netezza, vedi la [documentazione utente del database IBM Netezza](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
