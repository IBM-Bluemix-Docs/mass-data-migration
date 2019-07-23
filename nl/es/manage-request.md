---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

# Gestión de su solicitud
{: #manage-request}

Gestione y realice un seguimiento del estado de su pedido de {{site.data.keyword.mdms_full}} utilizando el
{{site.data.keyword.slportal}}.
{: shortdesc}

Si participa en el programa beta de {{site.data.keyword.mdms_short}}, puede obtener una vista previa de un nuevo panel de control de servicio de {{site.data.keyword.mdms_short}} al que puede acceder desde la consola de
{{site.data.keyword.cloud_notm}}. Para saber más, consulte [Obtención de acceso a la beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Seguimiento de su pedido 
{: #track-order}

Tras solicitar un dispositivo de almacenamiento, puede realizar el seguimiento del progreso de su pedido utilizando la
[página de detalles de la solicitud de {{site.data.keyword.mdms_short}}](https://control.softlayer.com/storage/mdms){: external} que está disponible desde el {{site.data.keyword.slportal}}.

En la tabla siguiente se muestra cómo cambia el estado del pedido a medida que {{site.data.keyword.mdms_short}} procesa la solicitud.

| Estado | Descripción |
| --- | --- |
| Procesando solicitud | Después de que {{site.data.keyword.mdms_short}} reciba la solicitud, el estado cambia a
_Procesando solicitud_. |
| Preparando dispositivo | Una vez que se apruebe el pedido, el estado de la solicitud cambia a _Preparando dispositivo_. {{site.data.keyword.mdms_short}} prepara y configura el siguiente dispositivo de almacenamiento disponible.  |
| Esperando envío | El dispositivo de almacenamiento preconfigurado está esperando el envío a su ubicación. Una vez que la solicitud entre en el estado _Esperando envío_, el pedido ya no se podrá cancelar. |
| Dispositivo enviado | El dispositivo de almacenamiento ha sido recogido por el transportista y se ha enviado a su ubicación. Puede ver el número de seguimiento en la sección _Detalles del pedido_ de la [página de detalles de la solicitud](https://control.softlayer.com/storage/mdms){: external}. |
| Dispositivo recibido | Una vez que se haya devuelto el dispositivo a {{site.data.keyword.cloud_notm}}, el estado cambia a
_Dispositivo recibido_. |
| Descargando datos | Durante el proceso de transferencia de datos, el estado de la solicitud cambia a
_Descargando datos_. El dispositivo se conecta a la red en el centro de datos de
{{site.data.keyword.cloud_notm}} y la descarga de datos se inicia automáticamente.  |
| Descarga completa| Cuando el proceso de descarga se haya completado, el estado de la solicitud cambiará a
_Descarga completa_. Los datos están ahora disponibles en el destino Cloud Object Storage que haya especificado en la solicitud inicial. |
| Borrado completo | {{site.data.keyword.mdms_short}} borra de forma permanente los datos del dispositivo utilizando los estándares de limpieza de datos NIST. Una vez que se haya completado el proceso de borrado de datos, el estado del pedido cambiará a
_Borrado completo_.
{: caption="Tabla 1. Descripción del flujo de trabajo del estado del pedido de {{site.data.keyword.mdms_short}}" caption-side="top"}
