---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Migration des bases de données Netezza vers DashDB

Le service Mass Data Migration Service (MDMS) peut être utilisé pour migrer de grandes bases de données Netezza vers DashDB.

Le présent document décrit :
- les outils Netezza qui permettent de déterminer la quantité de données à transférer à l'aide du service Mass Data Migration Service,
- les commandes qui permettent d'exporter ces données vers le périphérique Mass Data Migration.

## Dimensionnement de base de données
1. Depuis [IBM Support: Fix Central - Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}, téléchargez la version appropriée des outils Netezza qui correspond à votre instance Netezza.

   **REMARQUE** - Les outils de support sont installés par défaut sur le serveur Netezza dans le répertoire /nz/support-IBM_Netezza<version>/bin
   
2. Exécutez les deux commandes suivantes : `nz_db_size` et `nz_compressedTableRatio`

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

## Extraction de données et procédure d'intégration

Deux options permettent d'extraire les données de Netezza :
1. Utilisez l'utilitaire **nz_backup utility** :

   `/nz/support/contrib/bin/nz_backup –db   {db_name} –d  {répertoire_cible}  ascii threads 4`
   
   **REMARQUE **: {répertoire_cible} est le partage NFS fourni par le périphérique MDMS, monté sur ce serveur.
2. Utilisez CREATE EXTERNAL TABLE
   - Fournissez à l'équipe DashDB la clause “USING” utilisée pour l'exportation à des fins de réutilisation pendant le processus LOAD
   - Sélectionnez FORMAT = ”Text”
   
   
## Validation de données
Il est possible de relire les données sur Netezza en utilisant Select dans une table externe **myfile** `USING(....) “` pour garantir que les données sont correctes.
 
## Informations complémentaires 
Des informations complémentaires sur Netezza sont disponibles dans la [documentation utilisateur de base de données IBM Netezza](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
