---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# Verificación de los datos
{: #verify-data}

Puede acceder y verificar los datos migrados utilizando {{site.data.keyword.cos_full}}.
{: shortdesc}

Una vez finalizada la descarga, tendrá acceso inmediato a los datos en la nube mientras {{site.data.keyword.cloud_notm}} borra el dispositivo de forma segura.

## Acceso a los datos en Cloud Object Storage
{: #access-data-cos}

Los datos migrados están disponibles en la instancia de Cloud Object Storage que haya especificado al enviar su solicitud de
{{site.data.keyword.mdms_short}}. Antes de suprimir datos de su servidor de origen, verifique que los datos se hayan cargado correctamente en
{{site.data.keyword.cloud_notm}}.

Para acceder y verificar los datos: 

1. [Inicie sesión en la consola de {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Vaya a **Menú** &gt; **Lista de recursos** para ver una lista de sus recursos.
3. En la lista de recursos de {{site.data.keyword.cloud_notm}} seleccione su instancia suministrada de Cloud Object Storage.
4. En la lista de grupos de almacenamiento disponibles, seleccione el nombre del grupo que haya designado para la migración de datos.
5. Verifique que los objetos asociados al grupo corresponden a los datos que ha copiado en el dispositivo
{{site.data.keyword.mdms_short}}.

## Traslado de datos a una solución de almacenamiento distinta
{: #move-data}

Dependiendo de los requisitos de su carga de trabajo, es posible que necesite mover los datos migrados de Cloud Object Storage a una solución de almacenamiento en la nube distinta, como [Almacenamiento en archivo](https://{DomainName}/catalog/infrastructure/file-storage) o [Almacenamiento en bloque](https://{DomainName}/catalog/infrastructure/block-storage). 

Para obtener más información sobre las opciones de migración de almacenamiento, consulte
[Receta: mover datos de COS al almacenamiento en archivo o en bloque](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}.

