---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# Acerca de {{site.data.keyword.mdms_short}}
{: #about}

{{site.data.keyword.mdms_full}} es un método rápido, simple y seguro para transferir físicamente de terabytes a petabytes de datos a
{{site.data.keyword.cloud_notm}}.
{: shortdesc}

## ¿Por qué {{site.data.keyword.mdms_short}}?
{: #use-cases}

{{site.data.keyword.mdms_short}} le ayuda a simplificar su viaje a la nube proporcionando un dispositivo de almacenamiento preconfigurado y portátil para facilitar la migración de los datos. Obtenga más información sobre las características y casos de uso de
{{site.data.keyword.mdms_short}} en el vídeo siguiente.

<iframe class="embed-responsive-item" id="youtubeplayer" title="Mass Data Migration proporciona una forma fácil, simple y segura de transferir datos a IBM Cloud" type="text/html" width="100%" height="390" src="//www.youtube.com/embed/eNSlUoswvss?rel=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen> </iframe>


| Casos de uso| Descripción |
| --- | --- |
| Migración de los datos a la nube | Tanto si quiere liberar espacio de almacenamiento en sus instalaciones como archivar datos inactivos o realizar una copia de seguridad de los datos con fines de redundancia o recuperación, {{site.data.keyword.mdms_short}} puede mover sus datos a la nube de forma rápida y segura. |
| Retirada del centro de datos | Inicie la transformación de su centro de datos y utilice {{site.data.keyword.mdms_short}} para mover sus datos sensibles a la nube de forma segura, al tiempo que reduce, amplía o reubica su centro de datos. |
| Ancho de banda limitado | {{site.data.keyword.mdms_short}} es una gran alternativa si está en una ubicación remota o cree que las opciones por la red tienen un coste prohibitivo, son demasiado lentas o no están disponibles para su transferencia de datos. |
{: caption="Tabla 1. Describe los casos de uso de {{site.data.keyword.mdms_short}} " caption-side="top"}

Puede comparar sus opciones de migración de datos en {{site.data.keyword.cloud_notm}}
[explorando nuestras soluciones de migración de datos](https://www.ibm.com/cloud/data-migration). Para obtener más información sobre las características y ventajas de {{site.data.keyword.mdms_short}}, consulte la
[página del producto de {{site.data.keyword.mdms_short}}](https://www.ibm.com/cloud/mass-data-migration){: external}.
{: tip}

## Funcionamiento
{: #how-it-works}

{{site.data.keyword.mdms_short}} utiliza dispositivos de almacenamiento de una capacidad utilizable de 120 TB para acelerar el traslado de datos a la nube y superar los desafíos comunes, como altos costes de transferencia, tiempos de transferencia largos y problemas de seguridad.

En la imagen siguiente se describe el proceso de {{site.data.keyword.mdms_short}}.

![Describe el proceso de Mass Data Migration.](images/mdms-workflow.png)

## Componentes de servicio
{: #service-componenets}

{{site.data.keyword.mdms_short}} consta de los componentes de servicio siguientes.

<dl>
   <dt>Panel de control de {{site.data.keyword.mdms_short}}</dt>
      <dd>Puede crear y realizar un seguimiento de los pedidos de {{site.data.keyword.mdms_short}} desde el panel de control de servicio del
<a href="https://control.softlayer.com/" target="_blank" class="external">{{site.data.keyword.slportal}}</a>. En la página de solicitud de
{{site.data.keyword.mdms_short}}, debe especificar los valores de configuración de red para el dispositivo, recuperar las credenciales para iniciar sesión en el dispositivo y realizar el seguimiento del estado del pedido. </dd>
   <dt>Dispositivo {{site.data.keyword.mdms_short}}</dt>
      <dd>{{site.data.keyword.mdms_short}} proporciona un
<a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview">dispositivo de almacenamiento portátil</a> que se envía a su ubicación. El dispositivo {{site.data.keyword.mdms_short}} llega preconfigurado y listo para conectarse a la red.</dd>
   <dt>Interfaz de usuario del dispositivo</dt>
      <dd>La <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui">interfaz de usuario del dispositivo</a> es una interfaz de usuario local basada en web para puede utilizar para acceder al recurso compartido de red en el dispositivo
{{site.data.keyword.mdms_short}}. La interfaz de usuario se basa en software de archivos y de red maduro que permite que se pueda copiar y transportar un número elevado de archivos grandes a {{site.data.keyword.cloud_notm}}.</dd>
</dl>










