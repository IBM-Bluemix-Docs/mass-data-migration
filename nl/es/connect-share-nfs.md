---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount NFS share, NFS, access network share, connect to network share

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

# Conexión al recurso compartido de red utilizando NFS
{: #connect-nfs-share}

Para preparar la copia de datos, puede acceder al recurso compartido de red en el dispositivo
{{site.data.keyword.mdms_full}} utilizando el protocolo NFS (Network File System).
{: shortdesc}

Antes de conectarse al recurso compartido:

- Asegúrese de que tiene software NFS, como `nfs-common`, instalado en el cliente. Puede instalar el paquete
`nfs-common` ejecutando `sudo apt install nfs-common` desde la sesión de terminal.

## Gestión del acceso a la compartición NFS
{: #manage-nfs-share-access}

De forma predeterminada, el recurso compartido de red está configurado para tener acceso público. Antes de montar el recurso compartido en el servidor, puede añadir reglas de acceso NFS en el recurso compartido para ajustarse a sus requisitos de entorno o de seguridad. 

Para obtener información detallada acerca de cómo controlar el acceso a los recursos compartidos en el dispositivo de almacenamiento, consulte la
[Documentación de OSNEXUS QuantaStor](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}.
{: tip}

Para modificar el acceso a la compartición NFS:

1. [Inicie sesión en la interfaz de usuario del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. En el asistente Tareas comunes, pulse **Ver recursos compartidos de red** para mostrar la vista de recursos compartidos de red.

   ![Iconos de flujo de trabajos](images/workflow.png)
3. Cierre el asistente Tareas comunes y, a continuación, pulse el botón derecho del ratón sobre el nombre del recurso compartido de red para ver una lista de opciones. 
4. Pulse **Añadir acceso NFS** para modificar el acceso a la compartición NFS.

    ![Modificar el acceso a la compartición NFS](images/add-nfs-access.png)

## Montaje de la compartición NFS en un sistema Unix
{: #mount-nfs-share}

Tras desbloquear y activar la agrupación de almacenamiento en el dispositivo, puede conectarse a la compartición NFS en un sistema basado en Unix utilizando la interfaz de usuario del dispositivo {{site.data.keyword.mdms_short}}.

Para montar el recurso compartido de red: 

1. [Inicie sesión en la interfaz de usuario del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. En el asistente Tareas comunes, pulse **Ver recursos compartidos de red** para mostrar la vista de recursos compartidos de red.
3. Cierre el asistente Tareas comunes y, a continuación, pulse el botón derecho del ratón sobre el nombre del recurso compartido de red para ver una lista de opciones. 
4. Pulse **Ver mandato de montaje** para revisar la información de montaje de la compartición.

    En la imagen siguiente se muestra el recuadro de diálogo Ver mandato de montaje con valores de ejemplo.

    ![Montaje de la compartición](images/mount-command.png)

    El valor _Puerto de red_ corresponde al puerto de transferencia de datos del dispositivo
{{site.data.keyword.mdms_short}}. El valor _Mandato de montaje_ especifica el mandato que se utiliza para montar y conectarse a la compartición.
5. Haga ping a la dirección IP que aparece en el recuadro de diálogo para probar la conectividad de red entre su sistema y el dispositivo
{{site.data.keyword.mdms_short}}.

   Asegúrese de que la dirección IP corresponda al [puerto de transferencia de datos 10GbE](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings) del dispositivo.
   {: note}  
6. Copie el mandato de montaje que aparece en el recuadro de diálogo y pegue el mandato en una sesión de terminal de su sistema.
7. Ejecute el mandato para montar la compartición en su servidor.

## Siguientes pasos
{: #connect-nfs-share-next-steps}

- Inicie el [proceso de copia de datos](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data).
