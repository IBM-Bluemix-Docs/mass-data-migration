---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:codeblock: .codeblock}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Migration des bases de données Netezza vers DashDB
{: #migratingNetezzaDashDB}

Le service Mass Data Migration Service (MDMS) peut être utilisé pour migrer de grandes bases de données Netezza vers DashDB. Vous pouvez utiliser ce document comme référence pour les outils qui permettent de déterminer la quantité de données à transférer et les méthodes d'exportation.

## Détermination de la taille d'objet de base de données
1. Depuis [IBM Support > Fix Central > Netezza Tools ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}, téléchargez la version appropriée des outils Netezza qui correspond à votre instance Netezza.

   Les outils de support sont installés par défaut sur le serveur Netezza dans le répertoire `/nz/support-IBM_Netezza<version>/bin`
   {:note}

2. Exécutez les deux commandes suivantes :
   - `nz_db_size` pour déterminer la taille de la base de données.

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

   - `nz_compressedTableRatio` pour estimer la taille des données après compression.

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

## Extraction de données et processus d'intégration

Vous pouvez utiliser deux options pour extraire les données de Netezza.
- Utilisez l'utilitaire `nz_backup`.
   ```
   /nz/support/contrib/bin/nz_backup –db   {db_name} –d  {target_directory}  ascii threads 4
   ```

   `{target_directory}` est le partage NFS fourni par le périphérique MDMS et monté sur ce serveur.
   {:tip}

- Utilisez l'instruction `CREATE EXTERNAL TABLE`.
   - Sélectionnez `FORMAT` = ”Text”
   - Fournissez à l'équipe DashDB la clause `USING` utilisée pour l'exportation à des fins de réutilisation pendant le processus `LOAD`


## Validation des données
Il est possible de relire les données sur Netezza en utilisant l'instruction `SELECT FROM` dans une table externe `myfile` et une clause `USING(....)` pour garantir que les données sont correctes.

**Informations supplémentaires**

Pour plus d'informations sur Netezza, voir [la documentation relative à l'utilisation d'une base de données IBM Netezza ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
