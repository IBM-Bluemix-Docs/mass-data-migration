---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# Acceso a la interfaz de usuario del dispositivo
{: #access-ui}

Tras configurar el dispositivo {{site.data.keyword.mdms_full}} para la conectividad Ethernet, está listo para acceder a la interfaz de usuario del dispositivo para poder interactuar con el dispositivo e iniciar el proceso de migración de los datos.
{: shortdesc}

## Recuperación de las credenciales de dispositivo (beta)
{: #retrieve-device-credentials}

Al enviar una solicitud de {{site.data.keyword.mdms_short}}, el servicio genera automáticamente las credenciales en su nombre, que puede utilizar para acceder a la interfaz de usuario web local del dispositivo. 

Esta característica está disponible como parte del [release beta de {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). También puede acceder a las credenciales de su dispositivo de almacenamiento desde la sección _Detalles de la solicitud_ del [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Para recuperar las credenciales del dispositivo:

1. [Inicie sesión en la consola de {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Vaya a **Menú** &gt; **Lista de recursos** para ver una lista de sus recursos.
3. Desde la lista de recursos de {{site.data.keyword.cloud_notm}} seleccione su instancia suministrada de {{site.data.keyword.mdms_short}}.
4. En el separador _Detalles de la solicitud_, vaya a la sección Credenciales.
5. Copie los valores de **Nombre de usuario** y **Contraseña**.

## Inicio de sesión en la interfaz de usuario del dispositivo
{: #log-in-ui}

Utilice las credenciales que ha recuperado en el paso anterior para iniciar sesión en la interfaz de usuario web local e interactuar con el dispositivo {{site.data.keyword.mdms_short}}.

1. Abra un navegador web y acceda a la dirección IP estática que ha proporcionado en el formulario de pedido.

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Sustituya `<device_management_IP_address>` por la dirección IP configurada para los puertos de red Eth1 o Eth2. Acepte la excepción de certificado.

2. Inicie sesión en la interfaz de usuario del dispositivo utilizando el nombre de usuario y la contraseña que ha recuperado en el paso anterior. 

   ![Página de inicio de sesión](images/login.png)
   
   Aparecerá el asistente Tareas comunes. Utilice las opciones de izquierda a derecha para empezar a importar los datos.

   ![Iconos de flujo de trabajos](images/workflow.png)

   Puede volver a abrir el asistente Tareas comunes utilizando el **Gestor de trabajo** de la parte superior izquierda de la interfaz.
   {:tip}

## Siguientes pasos
{: #access-ui-next-steps}

- Para preparar la copia de ingestión de datos, empiece por [desbloquear la agrupación de almacenamiento en el dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool).
