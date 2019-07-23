---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# Resolución de problemas
{: #troubleshooting}

Los problemas generales con el uso de {{site.data.keyword.mdms_full}} pueden incluir la visualización del estado del pedido o el acceso a la interfaz de usuario. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{: shortdesc}

## No se ha podido conectar con la compartición SMB
{: #unable-to-mount-smb-share}

Al intentar montar la compartición SMB (Server Message Block) que se proporciona en el dispositivo
{{site.data.keyword.mdms_short}}, no puede conectarse a la compartición. 

Está utilizando el protocolo de transferencia de archivos SMB en un servidor Windows que se ha unido a un dominio de Active Directory. Para mover datos al dispositivo {{site.data.keyword.mdms_short}}, debe conectarse a la compartición de red que se proporciona en el dispositivo. Puede hacer ping a la dirección IP que corresponde al puerto de transferencia de datos de 10GbE en el dispositivo, pero no puede montar ni conectarse a la compartición desde el servidor.
{: tsSymptoms}

Tras unir el dispositivo {{site.data.keyword.mdms_short}} a Active Directory, el sistema habilita la firma SMB de forma predeterminada. La firma SMB añade seguridad adicional durante una comunicación de red eliminando la posibilidad de que se produzcan ataques de tipo man-in-the-middle.  No obstante, la firma SMB puede afectar al rendimiento de red de la transferencia de datos o provocar
[problemas al montar la compartición en el servidor](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}. 
{: tsCauses} 

Si no utiliza ni necesita la firma SMB en su entorno, puede inhabilitar la firma SMB en el cliente para evitar problemas de conexión y aumentar el rendimiento de la transferencia de datos.
{: tsResolve}

Para inhabilitar la firma SMB en un servidor Windows, establezca las claves de registro siguientes en cero:

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

Para obtener más información acerca de la firma SMB, consulte
[Visión general de la firma SMB (Server Message Block)](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}.

## No se pueden ver los detalles del pedido
{: #unable-to-view-order}

Al acceder a la consola de {{site.data.keyword.cloud_notm}}, no puede ver ni realizar un seguimiento de un pedido de
{{site.data.keyword.mdms_short}} para su organización.

Puede ver una lista de servicios en la lista de recursos de {{site.data.keyword.cloud_notm}}, pero no puede ver una entrada de
{{site.data.keyword.mdms_short}}.
{: tsSymptoms}

No tiene la autorización correcta para ver ni para realizar un seguimiento de los pedidos de
{{site.data.keyword.mdms_short}}.
{: tsCauses} 

Verifique con el administrador que se le haya asignado el rol correcto en el grupo de recursos o la instancia de servicio. Para obtener más información sobre los roles, consulte [Roles y permisos](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Obtención de ayuda y soporte
{: #getting-help}

Si tiene problemas o preguntas relacionados con el uso del dispositivo {{site.data.keyword.mdms_short}}, puede obtener ayuda buscando información en el Centro de soporte o directamente poniéndose en contacto con nosotros.

Para acceder al Centro de soporte, inicie una sesión en la consola de {{site.data.keyword.cloud_notm}} y pulse **Soporte** en la barra de menús.

Puede utilizar el campo de búsqueda del Centro de soporte para encontrar respuestas a sus preguntas en la documentación de {{site.data.keyword.cloud_notm}} y en el foro de Stack Overflow. También puede gestionar casos de soporte desde el Centro de soporte. Puede encontrar enlaces tanto al foro de Stack Overflow (para preguntas de carácter técnico) como al foro de IBM Developer Answers (para todos los demás tipos de preguntas) en la sección Foros del Centro de soporte.

Si tiene un [plan de soporte](/docs/get-support?topic=get-support-support-plans#support-plans) básico, avanzado o premium, podrá encontrar números de teléfono y una opción de chat para obtener ayuda.

El Centro de soporte es el método preferido para obtener ayuda, pero si no puede iniciar sesión en
{{site.data.keyword.cloud_notm}}, puede utilizar el
[Portal de servicio de {{site.data.keyword.cloud_notm}}](http://www.ibm.biz/bluemixsupport){: external} para enviar un caso.

Para obtener más información sobre cómo abrir una incidencia de soporte de {{site.data.keyword.IBM_notm}}, o acerca de los niveles de soporte y la gravedad de las incidencias, consulte [Cómo obtener soporte](/docs/get-support?topic=get-support-getting-customer-support){: external}.
