---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# Guía de aprendizaje de iniciación
{: #getting-started-tutorial}

{{site.data.keyword.mdms_full}} le ayuda a mover de terabytes a petabytes de datos a {{site.data.keyword.cloud_notm}} de una forma rápida, simple y segura. Esta guía de aprendizaje muestra cómo solicitar su dispositivo de migración utilizando el {{site.data.keyword.slportal}}.
{: shortdesc}

¿Está interesado en probar nuevas características de {{site.data.keyword.mdms_short}}? Puede obtener una vista previa de las próximas mejoras del servicio participando en el programa beta de {{site.data.keyword.mdms_short}}. Para saber más, consulte [Obtención de acceso a la beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: tip}

## Antes de empezar
{: #get-started-prereqs}

Antes de solicitar un dispositivo {{site.data.keyword.mdms_short}}:

- Planifique la migración revisando las [regiones y ubicaciones](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions) donde está disponible {{site.data.keyword.mdms_short}}.
- Asegúrese de tener suministrada una instancia de [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} para su cuenta de {{site.data.keyword.cloud_notm}}. 
- Debe conocer los tipos y velocidades de su conexión de red.
- Recopile sus valores de red, como las direcciones IP y otros detalles de direccionamiento, para conectar el dispositivo a su servidor de origen.
- Identifique una persona que pueda recibir, conectar y utilizar el dispositivo en su emplazamiento.

## Creación de un grupo de almacenamiento
{: #get-started-create-bucket}

Tras suministrar una instancia de Cloud Object Storage, cree un grupo de almacenamiento para establecer un destino para los datos migrados. 

1. Desde la lista de recursos de {{site.data.keyword.cloud_notm}} seleccione su instancia suministrada de Cloud Object Storage.
2. En la página _Iniciación_, pulse **Crear grupo**.
3. Especifique un nombre de grupo y seleccione una opción de resiliencia para los datos.
   
   La opción de resiliencia determina cómo distribuye los datos el servicio Cloud Object Storage a lo largo del área geográfica después de que los datos se importen en el servicio. {{site.data.keyword.mdms_short}} admite todas las opciones de resiliencia que están disponibles para Cloud Object Storage.  
   {: note}
4. En la lista de ubicaciones, seleccione el área geográfica donde desee que se almacenen físicamente los datos después de su migración al grupo de almacenamiento.
5. En la lista de clases de almacenamiento, seleccione **Estándar**.
6. Pulse **Crear grupo**.

## Solicitud de un dispositivo
{: #get-started-request-device}

Puede solicitar un dispositivo {{site.data.keyword.mdms_short}} utilizando el {{site.data.keyword.slportal}}.

1. Inicie sesión en el [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}.
2. En el menú de navegación, pulse **Almacenamiento** > **Migración de datos** > **{{site.data.keyword.mdms_short}}** para acceder a la página de destino de {{site.data.keyword.mdms_short}}.
3. Pulse **Solicitar dispositivo** para abrir el formulario de pedido.
4. Inicie su solicitud de {{site.data.keyword.mdms_short}} especificando los detalles siguientes.

    <table>
      <tr>
        <th>Acción</th>
        <th>Descripción</th>
      </tr>
      <tr>
        <td>Añadir un nombre de solicitud</td>
        <td>Especifique un alias para identificar y realizar el seguimiento de su solicitud de {{site.data.keyword.mdms_short}}.</td>
      </tr>
      <tr>
        <td>Seleccionar el destino de descarga de datos</td>
        <td>En la lista desplegable, seleccione su instancia suministrada de Cloud Object Storage. A continuación, seleccione el nombre que ha asignado al grupo de almacenamiento donde desea almacenar los datos migrados.</td>
      </tr>
      <tr>
        <td>Añadir una dirección de envío</td>
        <td>Especifique su información de envío, como la dirección de envío y el nombre de la persona que aceptará la entrega.</td>
      </tr>
      <tr>
        <td>Añadir contactos de migración</td>
        <td>Especifique el nombre de la persona que gestionará la migración de datos al dispositivo.</td>
      </tr>
      <tr>
        <td>Configurar valores de red</td>
        <td>
          <p>Configure los valores de la conexión de transferencia de datos especificando sus detalles de configuración de red.</p>
          <p>Proporcione los <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">valores de red</a> siguientes:</p>
          <p>
            <ul>
              <li><i>Valores de gestión de dispositivo.</i> Especifique la dirección IP estática y la pasarela predeterminada de su sistema remoto.</li>
              <li><i>Valores de transferencia de datos.</i> Especifique la dirección IP estática y la máscara de red del servidor donde residen los datos de origen.</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">Tabla 1. Describe el flujo de trabajo de solicitud de {{site.data.keyword.mdms_short}}</caption>
    </table>

    Al seleccionar una ubicación de entrega para su dispositivo, tenga en cuenta el peso del dispositivo y la accesibilidad. El dispositivo, junto con su maletín y una caja de transporte acolchada, pesa alrededor de 60 libras. Como ayuda en el transporte del dispositivo, la caja de transporte viene equipada con ruedas y un asa desplegable para que se pueda manejar fácilmente.
    {: tip}
5. Lea el acuerdo de servicios de {{site.data.keyword.mdms_short}} y, a continuación, marque el recuadro de selección.
6. Pulse **Realizar solicitud** para completar el pedido. 

## Qué hacer a continuación
{: #get-started-next-steps}

Se ha realizado correctamente. Ya ha completado la solicitud de {{site.data.keyword.mdms_short}}.

- Para obtener más información sobre cómo realizar el seguimiento del pedido, consulte [Gestión de la solicitud](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Para obtener más información sobre cómo recibir y conectar su dispositivo, consulte [Configuración del dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview).

