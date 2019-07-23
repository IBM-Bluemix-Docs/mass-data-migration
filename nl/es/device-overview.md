---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device models, device ports, network settings, configure network  

subcollection: mass-data-migration

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:external: target="_blank" .external}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Visión general del dispositivo
{: #device-overview}

{{site.data.keyword.mdms_full}} proporciona un dispositivo de almacenamiento preconfigurado y portátil que se envía a su ubicación para facilitar la migración de los datos.
{: shortdesc}

Utilice esta página para obtener información sobre las opciones de configuración de red para su dispositivo
{{site.data.keyword.mdms_short}}.

## Modelos de dispositivo
{: #device-models}

Su dispositivo {{site.data.keyword.mdms_short}} llega preconfigurado y listo para conectarse a la red. 

En la imagen siguiente se muestran las áreas principales del dispositivo.

<a href="https://{DomainName}/docs/api/content/mass-data-migration/images/mdms-device-rj45.svg">
  <img src="images/mdms-device-rj45.svg" alt="Vista de arriba a abajo del dispositivo Mass Data Migration">
</a>

{{site.data.keyword.cloud_notm}} proporciona dos modelos de dispositivo {{site.data.keyword.mdms_short}}. Cada modelo viene empaquetado con
[óptica y adaptadores](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-inventory-checklists) que admiten tanto conexiones de cobre SFP+ como RJ45. 

<table>
  <tr>
    <th>Modelo de dispositivo</th>
    <th>Descripción</th>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-RJ45-model">RJ45</a></p></td>
    <td>
      <ul>
        <li>Da soporte de forma nativa a la conectividad Ethernet utilizando conectores RJ45.</li>
        <li>Incluye adaptadores y óptica que habilitan el soporte de cobre SFP+.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td><p><a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-device#set-up-SFP+-model">RJ45 / SFP+</a></p></td>
    <td>
      <ul>
        <li>Da soporte de forma nativa a conexiones de cobre SFP+ y RJ45.</li>
      </ul>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tabla 1. Describe los modelos de dispositivo {{site.data.keyword.mdms_short}} soportados</caption>
</table>

Ambos modelos de dispositivo ofrecen las mismas funciones, pero las instrucciones de cableado son distintas para cada modelo. Al recibir su dispositivo {{site.data.keyword.mdms_short}}, asegúrese de identificar el modelo de dispositivo para poder seguir las instrucciones que correspondan a su tipo de dispositivo.  

Los dispositivos {{site.data.keyword.mdms_short}} utilizan un [cable de alimentación C13](https://en.wikipedia.org/wiki/IEC_60320){: external}. Si utiliza el dispositivo fuera de los Estados Unidos, es posible que necesite un adaptador de alimentación adicional que se ajuste al sistema de enchufe y zócalo que se utilice en su país. Los dispositivos {{site.data.keyword.mdms_short}} son compatibles con todos los rangos de alimentación estándar.
{: note}

## Puertos de dispositivo 
{: #network-settings}

Los dispositivos {{site.data.keyword.mdms_short}} están configurados para dos conexiones Ethernet. La primera conexión se encarga de la gestión del dispositivo mediante la ejecución de una interfaz de usuario basada en web, y la segunda conexión se encarga del movimiento de datos entre el dispositivo y su servidor de origen.

<dl>
    <dt>Puerto de gestión del dispositivo</dt>
        <dd>Puede gestionar el dispositivo {{site.data.keyword.mdms_short}} utilizando una interfaz de dispositivo local y basada en web que se utiliza en su sistema remoto. El puerto de gestión del dispositivo {{site.data.keyword.mdms_short}} proporciona acceso administrativo a la interfaz de usuario. Para ejecutar la interfaz de usuario, conecte su sistema al puerto de gestión del dispositivo y, a continuación, haga referencia a la dirección IP correspondiente en su navegador.</dd>
    <dt>Puerto de transferencia de datos</dt>
        <dd>El puerto de transferencia de datos se encarga del movimiento de datos de su sistema de almacenamiento al dispositivo
{{site.data.keyword.mdms_short}}. El puerto se ejecuta a una velocidad de 10GbE.</dd>
        <dd><p class="note">No hay soporte para la configuración de una pasarela tanto en el puerto de gestión del dispositivo como en el puerto de transferencia de datos. Si necesita configurar el direccionamiento en el puerto de transferencia de datos añadiendo una pasarela (no se recomienda), también deberá poder acceder a la dirección IP del puerto de transferencia de datos desde su navegador para ejecutar la interfaz de usuario del dispositivo.</p></dd>
</dl>

## Valores de red
{: #network-settings}

Los dispositivos {{site.data.keyword.mdms_short}} están configurados para su red en función de los valores que haya especificado al solicitar el dispositivo. Cuando solicite un dispositivo, puede especificar su configuración de red de acuerdo con los casos de ejemplo siguientes:

<dl>
    <dt>Configuración común</dt>
        <dd>En la mayoría de los casos, los dispositivos {{site.data.keyword.mdms_short}} se configuran designando el puerto 1GbE del dispositivo para la gestión del dispositivo y utilizando el puerto 10GbE para la transferencia de datos. Para el puerto de gestión del dispositivo, especifique la dirección IP estática, la máscara de red y la pasarela predeterminada para su sistema remoto. Para el puerto de transferencia de datos, debe especificar la dirección IP estática y la máscara de red del servidor con una pasarela y un puerto de datos 10GbE en la misma subred que el origen de datos. Esto se representa en el formulario de pedido.</dd>
    <dt>Configuración opcional</dt>
        <dd>También puede utilizar únicamente el puerto 10GbE del dispositivo tanto para la conexión de movimiento de datos como para la conexión de gestión del dispositivo. Al solicitar un dispositivo
{{site.data.keyword.mdms_short}}, puede especificar esta configuración en el formulario de pedido proporcionando la misma dirección IP estática, máscara de red y dirección de pasarela tanto para el puerto de gestión como para el puerto de datos. El dispositivo llega con el puerto 10GbE configurado con su información de IP, incluyendo una pasarela.</dd>
</dl>
