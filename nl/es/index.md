---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="DomainName"}

# Guía de inicio a la migración de datos masiva de {{site.data.keyword.cloud_notm}}
{: # GettingStarted}

**Requisitos previos**

Recopile esta información antes de enviar una solicitud de migración de datos masiva y completar la migración.

1. Valores de red del dispositivo de almacenamiento
   - Dirección IP estática
   - Máscara para habilitar la transferencia de datos
2. Valores de red del sistema remoto
   - Dirección IP estática
   - Máscara de red
   - Pasarela predeterminada para acceder a la interfaz de usuario
3. Destino de descarga de Cloud Object Storage <br/>

   Debe tener como mínimo una cuenta de {{site.data.keyword.cos_full}} y un grupo en varias regiones estándar de EE.UU. o de la UE cumplimentar el formulario de solicitud. Si todavía no dispone de una cuenta de {{site.data.keyword.cos_full_notm}}}, cree una antes de solicitar el dispositivo de migración de datos masiva. Consulte [Acerca de {{site.data.keyword.cos_full}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-about-ibm-cloud-object-storage){:new_window}.
   {:important}

## Creación de una solicitud

1. Inicie la sesión en la [consola de IBM Cloud](https://{DomainName}/){:new_window} y pulse el icono de menú de la parte superior izquierda. Seleccione **Infraestructura**.

   También puede iniciar la sesión en la [consola de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/catalog/){:new_window}.
2. Seleccione **Almacenamiento** > **Migración de datos** > **Migración de datos masiva** en la barra de navegación para acceder a la página de destino de la migración de datos masiva.
3. Pulse **Solicitar dispositivo** para abrir el formulario de pedido.
4. Rellene todos los campos del formulario de solicitud de **migración de datos masiva**.
   - **Dirección de envío**: este formulario no está rellenado de antemano y sus campos son editables. Proporcione el nombre de la persona que aceptará la entrega del dispositivo en el campo A la atención de. Cuando elija la ubicación de entrega, tenga en cuenta el peso del dispositivo (30 kg con el maletín) y la accesibilidad.

   El dispositivo está equipado con ruedas y un asa plegable para manejarlo con facilidad.
   {:note}

   - **Contactos clave de migración**: este formulario no está rellenado de antemano. Los campos son editables. Se puede añadir más de una persona.
   - **Configuración de red del centro de datos**: proporcione detalles sobre la configuración de red para el suministro previo del puerto Eth3 en el dispositivo de migración de datos masiva antes de envío.
   - **Destino de la descarga de datos**: seleccione la cuenta de destino de la lista.
   - **Nombre de la solicitud**: especifique un nombre para realizar el seguimiento del pedido.
5. Marque el recuadro de selección **He leído y acepto los términos del Acuerdo de migración de datos masiva** después de leer el acuerdo de cada servicio.
6. Pulse **Realizar solicitud** para enviar la solicitud. Pulse **Cancelar** para abandonar completamente el formulario y volver a la página de destino de la migración de datos masiva.


## Preparación y envío

Después de enviar la solicitud, el estado de la incidencia de solicitud aparece como `Procesando solicitud`. Una vez aceptada la solicitud, {{site.data.keyword.IBM}} comienza a preconfigurar el siguiente dispositivo disponible.

Cuando el dispositivo se esté preparando, el estado de la página [Solicitudes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/storage/mdms){:new_window} aparece como `Preparando dispositivo` seguido de `Pendiente de envío`. Después de pasar al estado `Pendiente de envío`, la solicitud ya no puede cancelarse.

Cuando el transportista recoge el dispositivo para enviarlo a su ubicación, el estado de solicitud se actualiza a `Dispositivo enviado`. Se le proporciona el número de seguimiento en el apartado **Detalles de la solicitud** de la página [Solicitudes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/storage/mdms){:new_window}.


## Recepción y conexión

1. El dispositivo estará preconfigurado cuando lo reciba. Se incluyen [instrucciones básicas para encenderlo y conectarlo](user-instructions.html). <br/>

   Se proporciona el nombre de usuario y la contraseña de la agrupación de almacenamiento por separado. Compruebe los **Detalles de la solicitud** en la página [Solicitudes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/storage/mdms){:new_window} para verificar las credenciales.
   {:note}
2. Apunte el navegador a la dirección IP estática proporcionada en el formulario de pedido.
3. Inicie una sesión y escriba la contraseña para desbloquear la agrupación de almacenamiento vacía. <br/>

   Consulte los detalles de la solicitud de su página [Solicitudes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/storage/mdms){:new_window} para ver la contraseña.
   {:tip}
4. Monte el recurso compartido NFS en el servidor.
5. Vuelva a ejecutar el inventario DataShuttle para asegurarse de que se han capturado los archivos nuevos.

## Movimiento de los datos
1. Ejecute la copia de DataShuttle para mover los datos.
2. Bloquee la agrupación de almacenamiento.
3. Cierre de forma adecuada el dispositivo de migración de datos masiva.
4. Devuelva la caja al centro de datos de {{site.data.keyword.BluSoftlayer_full}} con la etiqueta de envío suministrada.

Una vez que se devuelve el dispositivo a {{site.data.keyword.BluSoftlayer}}, el estado de la solicitud cambia a `Dispositivo recibido`.

## Descarga y acceso

Durante el proceso de transferencia, el estado de la solicitud se muestra como `Descargando datos`. El estado cambia de nuevo cuando finaliza la migración al grupo de {{site.data.keyword.objectstorageshort}} (`Descarga completada`). Se podrá acceder a los datos inmediatamente cuando se haya completado la descarga de alta velocidad al grupo Cloud Object Storage.

## Borrado del dispositivo

{{site.data.keyword.IBM}} implementa los requisitos de limpieza de datos de nivel DOD para borrar de forma permanente los datos del dispositivo. Cuando haya terminado, el estado de solicitud mostrará `Borrado completo`.
