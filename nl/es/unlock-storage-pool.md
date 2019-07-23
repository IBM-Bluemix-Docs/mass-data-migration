---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# Desbloqueo de la agrupación de almacenamiento
{: #unlock-storage-pool}

Puede copiar datos en el dispositivo {{site.data.keyword.mdms_full}} desbloqueando y activando en primer lugar la agrupación de almacenamiento que se suministra para el dispositivo.
{: shortdesc}

## Recuperación de la frase de contraseña de la agrupación de almacenamiento (beta)
{: #retrieve-storage-pool-passcode}

Para acceder a la agrupación de almacenamiento en el dispositivo {{site.data.keyword.mdms_short}}, recupere las credenciales del dispositivo accediendo a los detalles de la solicitud de
{{site.data.keyword.mdms_short}} en la consola de {{site.data.keyword.cloud_notm}}.

Esta característica está disponible como parte del
[release beta de {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). También puede acceder a las credenciales de su dispositivo de almacenamiento desde la sección _Detalles de la solicitud_ del [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Para recuperar la contraseña de la agrupación de almacenamiento:

1. [Inicie sesión en la consola de {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Vaya a **Menú** &gt; **Lista de recursos** para ver una lista de sus recursos.
3. Desde la lista de recursos de {{site.data.keyword.cloud_notm}} seleccione su instancia suministrada de {{site.data.keyword.mdms_short}}.
4. En el separador _Detalles de la solicitud_, vaya a la sección Credenciales.
5. Copie el valor de **Código de acceso de bloqueo de agrupación**.

## Activación de la agrupación de almacenamiento
{: #activate-storage-pool}

Desbloquee la agrupación de almacenamiento vacía utilizando las credenciales que ha recuperado en el paso anterior.

1. [Inicie sesión en la interfaz de usuario del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. En el asistente Tareas comunes, pulse **Desbloquear e iniciar agrupación de almacenamiento**.
3. Especifique la frase de contraseña de la agrupación de almacenamiento que ha recuperado en el paso 1 y, a continuación, pulse
**Aceptar**.
      
   ![Activar agrupación de almacenamiento](/images/StartStoragePool.png)

   De forma predeterminada, el recurso compartido tiene habilitados los protocolos NFS (Network File System) y SMB (Server Message Block) sin restricciones de acceso. Puede modificar el acceso a esta compartición para NFS o SMB pulsando el botón derecho del ratón sobre el nombre de la compartición en la interfaz de usuario y seleccionando luego la opción de menú adecuada.
   {: note}

## Siguientes pasos
{: #unlock-storage-pool-next-steps}

- Si utiliza una máquina Unix, [conéctese al recurso compartido de red utilizando NFS](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share).
- Si utiliza una máquina Windows,
[conéctese al recurso compartido de red utilizando SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share).
- Inicie el [proceso de copia de datos](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy).
