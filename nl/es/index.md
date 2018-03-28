---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Guía de inicio a la migración de datos masiva de {{site.data.keyword.cloud_notm}}

## Qué es necesario para solicitar un dispositivo

1. Valores de red del dispositivo de almacenamiento
   - Dirección IP estática
   - Máscara para habilitar la transferencia de datos
2. Valores de red del sistema remoto
   - Dirección IP estática
   - Máscara de red 
   - Pasarela predeterminada para acceder a la interfaz de usuario
3. Destino de descarga de Cloud Object Storage <br/>
   **Importante**: Debe tener como mínimo una cuenta de {{site.data.keyword.cos_full}} y un grupo en varias regiones de EE. UU. o en una ubicación del sur de EE. UU. para cumplimentar el formulario de solicitud. Si todavía no dispone de una cuenta de {{site.data.keyword.cos_full_notm}}}, cree una antes de solicitar el dispositivo de migración de datos masiva. Consulte [Acerca de {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Paso 1: Crear una solicitud

1. Acceda al [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} utilizando sus credenciales exclusivas.
2. Seleccione **Almacenamiento** > **Migración de datos** > **Migración de datos masiva** en la barra de navegación para acceder a la página de destino de la migración de datos masiva. <br/>
![Opción Servicio de transferencia de datos en el menú del portal de clientes](/images/DTSinControlMenu.PNG) <br/>
3. Pulse el enlace **Solicitar dispositivo** para abrir el formulario de pedido.
4. Rellene todos los campos del formulario de solicitud de **migración de datos masiva**.
   - **Dirección de envío**: este formulario no se rellena previamente y sus campos son editables. Proporcione el nombre de la persona que aceptará la entrega del dispositivo en el campo A la atención de. Al escoger la ubicación de entrega, tenga en cuenta el peso del dispositivo (30 kg con el maletín) y la accesibilidad. <br/> (**Nota**: el dispositivo está equipado con ruedas y un asa para poder moverlo).
   - **Contactos de migración clave**: este formulario no se rellena previamente. Los campos son editables. Se puede añadir más de una persona. 
   - **Configuración de red del centro de datos**: proporciona detalles sobre la configuración de red para el suministro previo del puerto Eth3 en el dispositivo de migración de datos masiva antes de envío.
   - **Destino de la descarga de datos**: seleccione la cuenta de destino de la lista desplegable.
   - **Nombre de la solicitud**: especifique un nombre para realizar el seguimiento del pedido.
5. Marque el recuadro de selección **He leído y acepto los términos del Acuerdo de migración de datos masiva** después de leer los acuerdos de servicio proporcionados.
6. Pulse **Realizar solicitud** para enviar la solicitud. Pulse **Cancelar** para abandonar completamente el formulario y volver a la página de destino de la migración de datos masiva.


## Paso 2: Preparación y envío

Después de enviar la solicitud, el estado de la incidencia de solicitud aparecerá como *Procesando solicitud*.  Una vez que se haya procesado la solicitud, {{site.data.keyword.IBM}} empezará a preconfigurar el siguiente dispositivo disponible y el estado en la cuadrícula [Solicitudes](https://control.softlayer.com/storage/mdms){:new_window} aparecerá como *Preparando dispositivo* seguido de *Esperando envío*.

Una vez que se acepte el pedido y el dispositivo se esté preparando, el estado de la cuadrícula [Solicitudes](https://control.softlayer.com/storage/mdms){:new_window} aparecerá como *Preparando dispositivo* seguido de *Pendiente de envío*. Cuando pasa al estado *Pendiente de envío*, la solicitud ya no puede cancelarse. 

Cuando el transportista recoge el dispositivo para enviarlo a su ubicación, el estado de solicitud se actualiza a *Dispositivo enviado*. Se le proporcionará el número de seguimiento en el apartado **Detalles de la solicitud** de la cuadrícula [Solicitudes](https://control.softlayer.com/storage/mdms){:new_window}.


## Paso 3: Recibir y conectar

1. El dispositivo estará preconfigurado cuando lo reciba. Se incluirán [instrucciones básicas para encenderlo y conectarlo](user-instructions.html). <br/>
  **Nota**: se proporcionará el nombre de usuario y la contraseña de la agrupación de almacenamiento por separado. Compruebe los **Detalles de la solicitud** en la cuadrícula [Solicitudes](https://control.softlayer.com/storage/mdms){:new_window} para las credenciales.
2. Apunte el navegador a la dirección IP estática proporcionada en el formulario de pedido.
3. Inicie sesión y proporcione la contraseña para desbloquear la agrupación de almacenamiento vacía. <br/>
   **Nota**: Consulte los detalles de la solicitud de su cuadrícula [Solicitudes](https://control.softlayer.com/storage/mdms){:new_window} para ver la contraseña.
4. Monte el recurso compartido NFS en el servidor.
5. Vuelva a ejecutar el inventario DataShuttle para asegurar que se hayan capturado los archivos nuevos que creados desde la aplicación.

## Paso 4: Recibir y conectar
1. Ejecute la copia de DataShuttle para mover los datos.
2. Bloquee la agrupación de almacenamiento.
3. Cierre de forma adecuada el dispositivo de migración de datos masiva.
4. Devuelva la caja al centro de datos de {{site.data.keyword.BluSoftlayer_full}} mediante la etiqueta que se proporciona para el envío.

Una vez que se devuelve el dispositivo a {{site.data.keyword.BluSoftlayer}}, el estado de la solicitud cambia a *Dispositivo recibido*. 

## Paso 5: Descarga y acceso

Durante el proceso de transferencia, el estado de la solicitud se muestra como *Descargando datos*. El estado cambia de nuevo cuando finaliza la migración al depósito de {{site.data.keyword.objectstorageshort}} (*Descarga completada*). Se podrá acceder a los datos inmediatamente una vez que se haya completado la descarga de alta velocidad al grupo Cloud Object Storage.

## Paso 6: Borrar el dispositivo

{{site.data.keyword.IBM}} implementará los requisitos de limpieza de datos de nivel DOD para borrar de forma permanente los datos del dispositivo. Cuando haya terminado, el estado de solicitud mostrará *Borrado completo*.

## Notas adicionales

### Exclusividad en el grupo

Para garantizar que los nombres de objetos son únicos cuando se copian en el grupo, se incluye un prefijo en el nombre de objeto de la vía de acceso; `/root/user/config.ini` se convierte en "root/user/config.ini" cuando se copia en el grupo.

### Grupos

Si el grupo de destino no existe, se crea.   Si existe, debe estar vacío; de lo contrario la copia no puede continuar.  

### Sistemas de archivos

Los enlaces simbólicos y los enlaces fijos se omiten durante el proceso de exploración.
