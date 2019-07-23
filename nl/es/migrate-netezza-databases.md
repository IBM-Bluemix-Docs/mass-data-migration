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

# Migración de bases de datos de PureData System for Analytics a {{site.data.keyword.dashdbshort_notm}}
{: #migrate-netezza-databases}

Se puede utilizar {{site.data.keyword.mdms_full}} para migrar bases de datos grandes de IBM PureData™ System for Analytics (basado en la tecnología de Netezza®) a {{site.data.keyword.dashdbshort}}. Puede utilizar este documento como referencia para las herramientas que determinan la cantidad de datos que se van a transferir y los métodos de exportación.
{: shortdesc}

## Determinación del tamaño del objeto de base de datos
{: #determine-db-object-size}

1. Desde [IBM Support > Fix Central > Netezza Tools ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}, descargue la versión adecuada de Netezza Tools correspondiente a su instancia de Netezza.

   De forma predeterminada, las herramientas de soporte se instalan en el servidor Netezza en el directorio
`/nz/support-IBM_Netezza<version>/bin`
   {:note}

2. Ejecute los siguientes mandatos.
   - `nz_db_size` para determinar el tamaño de la base de datos

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

   - `nz_compressedTableRatio` para estimar el tamaño de los datos cuando se descompriman.

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

## Extracción de datos e incorporación
{: #extract-data}

Dispone de dos opciones para extraer los datos de Netezza.
- Utilizar el programa de utilidad `nz_backup`.
   ```
   /nz/support/contrib/bin/nz_backup –db   {nombre_bd} –d  {directorio_destino}  ascii threads 4
   ```

   El `{directorio_destino}` es el recurso compartido NFS que proporciona el dispositivo MDMS y que está montado en este servidor.
   {:tip}

- Utilizar la sentencia `CREATE EXTERNAL TABLE`.
   - Seleccione `FORMAT` = ”Text”
   - Proporcione al equipo {{site.data.keyword.dashdbshort_notm}} la cláusula `USING` utilizada para exportar para reutilización durante el proceso `LOAD`.


## Validación de los datos
{: #validate-data}

Los datos se pueden volver a leer en Netezza mediante la sentencia `SELECT FROM` con la tabla externa `myfile` y una cláusula `USING(....)` para asegurarse de que los datos sean correctos.

**Información adicional**

Encontrará más información sobre PureData System for Analytics en la [documentación de usuario de la base de datos IBM Netezza ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
