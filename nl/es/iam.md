---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: user permissions, manage access, IAM roles

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

# Permisos de acceso de usuario
{: #manage-access}

{{site.data.keyword.mdms_full}} da soporte a un sistema de control de acceso centralizado, controlado por
{{site.data.keyword.iamlong}}, para ayudarle a gestionar los usuarios y el acceso a su solicitud de
{{site.data.keyword.mdms_short}} desde la consola de {{site.data.keyword.cloud_notm}}.
{: shortdesc}

Esta función está disponible como parte del release beta de {{site.data.keyword.mdms_short}}. Para obtener más información sobre cómo participar en el programa beta, consulte [Obtención de acceso a la beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: note}

## Roles y permisos
{: #roles}

Como propietario de la cuenta, puede establecer políticas dentro de su cuenta de
{{site.data.keyword.cloud_notm}} para crear distintos niveles de acceso para los distintos usuarios. Tras crear una solicitud de
{{site.data.keyword.mdms_short}}, puede decidir quién puede realizar el seguimiento del progreso del pedido desde la consola de
{{site.data.keyword.cloud_notm}}.

En la tabla siguiente se muestra cómo se correlacionan las acciones de {{site.data.keyword.mdms_short}} con los
[roles de gestión de plataforma de {{site.data.keyword.cloud_notm}} IAM](/docs/iam?topic=iam-userroles#iamusermanrol). 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>Rol de gestión de plataforma</th>
    <th>Descripción</th>
    <th>Acciones de ejemplo</th>
  </tr>
  <tr>
    <td><p>Visor</p></td>
    <td><p>Un visor solo tiene acceso de visualización a las instancias de servicio dentro de una cuenta de
{{site.data.keyword.cloud_notm}}. Los visores no pueden crear ni modificar instancias de servicio.</p></td>
    <td>
      <p>
        <ul>
          <li>Acceder a la página de detalles de la solicitud de {{site.data.keyword.mdms_short}}</li>
          <li>Ver el estado de un pedido de {{site.data.keyword.mdms_short}}</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Operador</p></td>
    <td><p>Un operador puede ver instancias de servicio, así como gestionar alias, enlaces y credenciales de servicio.</p></td>
    <td>
      <p>
        <ul>
          <li>No aplicable</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Editor</p></td>
    <td><p>Un editor tiene permisos más allá del rol de operador, incluyendo la posibilidad de crear y suprimir instancias de servicio.</p></td>
    <td>
      <p>
        <ul>
          <li>Crear una solicitud de {{site.data.keyword.mdms_short}}.</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Administrador</p></td>
    <td><p>Un administrador puede realizar todas las acciones que puede realizar un visor, un operador y un editor, incluyendo la posibilidad de invitar a nuevos usuarios y asignar políticas de acceso para otros usuarios.</p></td>
    <td>
      <p>
        <ul>
          <li>Todas las acciones que puede realizar un visor, un operador y un editor</li>
          <li>Asignar políticas de acceso de usuario</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tabla 1. Describe cómo los roles de acceso e identidad se correlacionan con los permisos de {{site.data.keyword.mdms_short}}</caption>
</table>

Para obtener información sobre cómo asignar roles de usuario en la interfaz de usuario, consulte
[Gestión del acceso a recursos](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}



