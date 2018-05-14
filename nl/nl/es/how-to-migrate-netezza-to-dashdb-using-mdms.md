---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Migración de bases de datos Netezza a DashDB

El servicio de migración de datos masiva (MDMS) puede utilizarse para migrar bases de datos grandes de Netezza a DashDB.

En este documento se describen:
- las herramientas de Netezza para determinar la cantidad de datos que se transfieren mediante el servicio de migración de datos masiva
- los mandatos para exportar los datos al dispositivo de migración de datos masiva.

## Dimensionamiento de la base de datos
1. Descargue la versión de Netezza Tools que corresponda a su instancia de Netezza en [Soporte de IBM: Fix Central-Netezza Tools](https://www-945.ibm.com/support/fixcentral/options?selectionBean.selectedTab=find&selection=ibm%2fInformation+Management%3bPureData+System+for+Analytics%3bibm%2fInformation+Management%2fNetezza+Tools){:new_window}.

   **NOTA:** las herramientas de soporte se instalan de forma predeterminada en el servidor Netezza en el directorio /nz/support-IBM_Netezza<version>/bin
   
2. Ejecute los dos mandatos siguientes: `nz_db_size` and `nz_compressedTableRatio`

```
nz_db_size
Objeto | Nombre | Bytes | KB | MB | GB | TB
-----------------------------------------------------------------------------------------------------------
Dispositivo | cdcntze1 | 23,388,712,337,408 | 22,840,539,392 | 22,305,214 | 21,782.4 | 21.3
Base de datos | DHDB | 183,537,500,160 | 179,235,840 | 175,035 | 170.9 | .2
Tabla | DH71964I1 | 880,803,840 | 860,160 | 840 | .8 | .0
Tabla | DH71964T1 | 96,120,078,336 | 93,867,264 | 91,667 | 89.5 | .1
Tabla | DH71964T10 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T2 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T3 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T4 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T5 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T6 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T7 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T8 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
Tabla | DH71964T9 | 9,615,179,776 | 9,389,824 | 9,170 | 9.0 | .0
```
```
nz_compressedTableRatio
....................................................................................
. Los valores siguientes muestran la proporción de tamaño de una tabla comprimida respecto al .
. formato no comprimido. Una tabla sin comprimir es aproximadamente <ratio> veces mayor .
. que cuando está comprimida. .
. .
. El 'Tamaño comprimido' es la cantidad real de almacenamiento que utiliza la tabla. .
. El 'Tamaño sin comprimir' es una estimación basada en cálculos matemáticos. .
....................................................................................
Base de datos: DHDB
Nombre de tabla/MView Proporción Tamaño comprimido Tamaño sin comprimir Diferencia de tamaño
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
Total para esta base de datos 1.50 183,537,500,160 275,251,242,240 91,713,742,080
```

## Procedimiento de extracción e incorporación de datos

Se pueden utilizar dos opciones para extraer los datos de Netezza:
1. Utilice la **utilidad nz_backup**:

   `/nz/support/contrib/bin/nz_backup –db   {nombre_bd} –d  {directorio_destino}  ascii threads 4`
   
   **NOTA**: Tenga en cuenta que el {directorio_destino} es el recurso compartido NFS proporcionado por el dispositivo MDMS montado en este servidor.
2. Utilice CREATE EXTERNAL TABLE
   - Proporcione al equipo DashDB la cláusula "USING" utilizada para la exportación para reutilizarla durante el proceso LOAD
   - Seleccione FORMAT = ”Text”
   
   
## Validación de datos
Los datos se pueden releer en Netezza mediante la opción de selección de la tabla externa de **myfile** `USING (....) “` para garantizar que los datos sean correctos.
 
## Información adicional
Hay más información disponible sobre Netezza en la [documentación de usuario de la base de datos de IBM Netezza](https://www.ibm.com/support/knowledgecenter/en/SSULQD_7.2.1/com.ibm.nz.dbu.doc/c_dbuser_plg_overview.html){:new_window}.
