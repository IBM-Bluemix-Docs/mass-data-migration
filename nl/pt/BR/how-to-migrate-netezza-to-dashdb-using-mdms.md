---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Migrando bancos de dados do Netezza para o DashDB

O Mass Data Migration Service (MDMS) pode ser usado para migrar grandes bancos de dados do Netezza para o DashDB.

Este documento descreve:
- as ferramentas do Netezza para determinar a quantia de dados que deve ser transferida por meio do Mass Data Migration Service.
- os comandos para exportação dos dados no dispositivo do Mass Data Migration.

## Dimensionamento do banco de dados
1. No [Suporte IBM: Fix Central - Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}, faça o download da versão apropriada do Netezza Tools que corresponda à sua instância do Netezza.

   **NOTA** - por padrão, ferramentas de suporte são instaladas no servidor Netezza no diretório /nz/support-IBM_Netezza<version>/bin
   
2. os dois comandos a seguir: `nz_db_size` e `nz_compressedTableRatio`

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

## Extração de dados e procedimento de migração

Há duas opções que podem ser usadas para extrair os dados do Netezza:
1. Usar o **nz_backup utilitário**:

  ```
  /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
  ```
   
   **NOTA**: observe que o {target_directory} é o compartilhamento do NFS fornecido pelo dispositivo MDMS, montado nesse servidor.
   
2. Usar CREATE EXTERNAL TABLE
   - Forneça à equipe do DashDB a cláusula "USING" para exportar para reutilização durante o processo LOAD
   - Selecione FORMAT = ”Text”
   
   
## Validação de dados
Os dados podem ser lidos novamente no Netezza usando selecionar na tabela externa **myfile** `USING(....) “` para assegurar que os dados estejam corretos.
 
## Informações adicionais
Mais informações sobre o Netezza estão disponíveis na [Documentação do usuário do banco de dados do IBM Netezza](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
