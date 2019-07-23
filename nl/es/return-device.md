---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# Devolución del dispositivo
{: #return-device}

Apague y devuelva su dispositivo {{site.data.keyword.mdms_full}} a {{site.data.keyword.cloud_notm}} para completar el proceso de migración.
{: shortdesc}

## Desconexión del dispositivo
{: #disconnect-device}

Cuando el proceso de copia de datos se complete, puede apagar correctamente el sistema.

1. En el asistente Tareas comunes, pulse **Cerrar dispositivo**.

    ![Cierre del dispositivo](images/ShutDown.png)

    Pulse **Aceptar** para confirmar.
2. Apague el dispositivo utilizando el botón **Encender/Apagar el sistema** del dispositivo. 
3. Establezca el **Interruptor de alimentación** en **Desactivado**.
4. Agrupe y devuelva todos los cables y toda la óptica a sus ubicaciones de almacenamiento dentro del maletín de transporte.

## Envío del dispositivo a {{site.data.keyword.cloud_notm}}
{: #ship-device}

Prepare la etiqueta de envío y avise al transportista cuando esté listo para devolver el dispositivo.

1. Recupere la lista de inventario y la etiqueta de envío de devolución del dispositivo. Estos documentos se encuentran bajo la tapa del maletín de transporte.

    Si va enviar varios dispositivos, tenga en cuenta que la etiqueta de envío de devolución que se incluye en cada maletín es específica del dispositivo de almacenamiento. Antes de planificar la recogida con el transportista, asegúrese de que la etiqueta de envío de devolución correspondiente esté fijada en el dispositivo adecuado. 
    {: note}
2. Utilice la lista de inventario para verificar que todos los cables y toda la óptica se devuelven y almacenan en el maletín de transporte.
3. Devuelva la lista de inventario al maletín de transporte y, a continuación, utilice las instrucciones que aparecen en la etiqueta de envío de devolución para fijar la etiqueta al dispositivo.
4. Planifique la recogida con el transportista y devuelva el dispositivo al centro de datos.

    Cuando se devuelve un dispositivo a {{site.data.keyword.cloud_notm}}, el estado del pedido cambia a _Dispositivo recibido_ en la página de detalles de solicitud de {{site.data.keyword.mdms_short}}.

## Siguientes pasos
{: #return-device-next-steps}

- Compruebe el estado del pedido [gestionando la solicitud de {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Antes de suprimir datos de su servidor de origen, [verifique que los datos se hayan cargado correctamente en {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data).

