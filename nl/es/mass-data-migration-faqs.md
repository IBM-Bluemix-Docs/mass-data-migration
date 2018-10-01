---

copyright:
  years: 2017, 2018
lastupdated: "2018-09-19"

---
{:new_window: target="_blank"}

# Preguntas más frecuentes

## **¿Qué es la migración de datos masiva de {{site.data.keyword.cloud_notm}}?**

La migración de datos masiva de {{site.data.keyword.cloud}} es un servicio de transferencia de datos físicos que acelera el traslado seguro de terabytes a petabytes de datos en {{site.data.keyword.cloud_notm}} mediante dispositivos de almacenamiento robustos y portátiles de 120 TB de capacidad utilizable.

<hr/>

## **¿Cómo se inicia la migración de datos masiva?**

Utilice [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} para enviar la solicitud. Cuando dicha solicitud se haya aprobado y procesado, se preconfigura el siguiente o los siguientes dispositivos disponibles y se le envían de acuerdo con la información de red y de envío que haya especificado. Utilice el enlace siguiente para empezar ahora: https://control.softlayer.com/storage/mdms

<hr/>

## **¿Por qué utilizar la migración de datos masiva?**

Los dispositivos de migración de datos masiva están equipados para rendir en casi cualquier entorno desde los centros de datos y oficinas hasta lugares remotos, almacenes y barcos. La migración de datos masiva también es una alternativa si las opciones por la red tienen un coste prohibitivo, son demasiado lentas o no están disponibles.

<hr/>

## **¿Cuántos datos se pueden transferir mediante la migración de datos masiva?**

No hay prácticamente ningún límite por lo que respecta a la cantidad de datos que se pueden transferir, tanto si son algunos terabytes como si son petabytes. Cada dispositivo tiene hasta 120 TB de capacidad utilizable en RAID-6, pero se pueden utilizar varios dispositivos para acomodar cargas de trabajo más grandes. El tamaño máximo de un solo objeto es 10 TB.

<hr/>

## **¿Se pueden utilizar varios dispositivos para mover cargas de trabajo que superen los 120 TB? De ser así, ¿cómo se hace?**

Se utilizan varios dispositivos en paralelo o en serie para mover todos los datos en una sola migración o bien se utiliza un único dispositivo en migraciones iterativas. Por ejemplo, se pueden transferir de 1 PB de datos utilizando nueve dispositivos en paralelo o bien utilizar un único dispositivo para hacer nueve migraciones distintas.

<hr/>

## **¿Cuánto tardan en transferirse los datos?**

Desde el momento en que un cliente envía una solicitud de migración de datos masiva hasta el momento en que sus datos son accesibles en su grupo de {{site.data.keyword.cos_full}}, pueden pasar tan solo siete días. El rendimiento de la transferencia se ve afectado por el número de archivos que hay que transferir. Se tarda más en transferir millones de archivos pequeños que en transferir la misma cantidad de datos contenidos en pocos archivos.

<hr/>

## **¿Durante cuánto tiempo se puede mantener el dispositivo de migración de datos masiva?**

Un dispositivo puede estar en unas instalaciones sin coste alguno durante los primeros 10 días hábiles. Este periodo de tiempo no incluye el día se envía el dispositivo ni el día que lo recibe. Si se necesita más tiempo para completar la ingesta, se puede prorrogar su uso por 30 dólares al día a partir del undécimo día (se aplica a EE.UU. y la UE).

<hr/>

## **¿Qué interfaces de red admite la migración de datos masiva?**

Los dispositivos de migración de datos masiva tienen interfaces de red con 10 Gbps con puertos de red de cobre SFP+ y RJ45 (CAT6a). También se incluye el convertidor de RJ45 a SFP+. Las interfaces de 10 Gbps tienen habilitadas las tramas Jumbo.

<hr/>

## **¿Qué es la opción de envío predeterminado de la migración de datos masiva?**

La migración de datos masiva utiliza la entrega de envío y devolución UPS Next Day Air para enviar todos los dispositivos. El coste se incluye en la tarifa baja y plana de 395 dólares por dispositivo. Por ahora, los clientes no pueden seleccionar otro método de envío.

<hr/>

## **¿En qué regiones está disponible la migración de datos masiva?**

Actualmente la migración de datos masiva solo está disponible en Estados Unidos y en la Unión Europea. Todos los datos se migran a {{site.data.keyword.cos_full}} en los niveles de servicio de varias regiones estándar de EE.UU. o de la UE. Los dispositivos no se pueden enviar desde una región y devolverse en otra.

<hr/>

## **¿Cuánto cuesta importar datos en {{site.data.keyword.cloud_notm}}?**

No se aplica ningún cargo por transferir datos a {{site.data.keyword.cloud_notm}}.

<hr/>

## **¿Se puede utilizar la migración de datos masiva para exportar datos de {{site.data.keyword.cloud_notm}}?**

Por ahora, la migración de datos masiva no admite la exportación de datos fuera del {{site.data.keyword.cloud_notm}}.

<hr/>

## **¿La migración de datos masiva cifra los datos?**

La migración masiva de datos cifran todos los datos con el cifrado AES de 256 bits y proporciona una contraseña fuerte para desbloquear la agrupación de almacenamiento. Todas las transferencias de datos de {{site.data.keyword.IBM}} se realizan por SSL.

<hr/>

## **¿Cómo protege los datos físicamente la migración de datos masiva?**

Todos los dispositivos de migración de datos masiva se alojan en compartimentos robustos y duraderos. Los compartimentos son impermeables, a prueba de golpes y con detección de manipulaciones para garantizar el envío y la devolución del dispositivo, así como la seguridad de los datos.

<hr/>

## **¿Cómo puedo solicitar que se realice el seguimiento durante el proceso de migración?**

Para realizar el seguimiento del estado de una solicitud, consulte el apartado de solicitudes activas en la página de migración de datos masiva de [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. También puede iniciar la sesión en el portal mediante el enlace siguiente: https://control.softlayer.com/storage/mdms

<hr/>

## **¿Cómo se borran los datos después de que se descarguen en {{site.data.keyword.cos_full_notm}}?**

Una vez que se ha completado el traspaso de datos a {{site.data.keyword.cos_full}}, {{site.data.keyword.IBM}} inicia inmediatamente una limpieza de datos de nivel DOD para borrar los datos del dispositivo de forma permanente.

<hr/>

## **¿Cuál es la interfaz de archivos?**

El dispositivo de migración de datos masiva tiene recursos compartidos con NFS (sistema de archivos de red) y SMB (bloque de mensajes de servidor) habilitados de forma predeterminada.

<hr/>

## **¿Cómo se utiliza la interfaz de archivos?**

En primer lugar, desbloquee la agrupación de cifrado. A continuación, monte el recurso compartido en el servidor que contiene los datos que desea migrar. Empiece a copiar los archivos de datos en el recurso compartido.

<hr/>

## **¿Qué ventajas tiene la interfaz de archivos de la migración de datos masiva?**

La interfaz de archivos se basa en un archivo maduro y software de red que permite copiar y mover un gran número de archivos grandes a {{site.data.keyword.cloud_notm}}.

<hr/>

## **¿Cómo se almacenan los archivos en el dispositivo de migración de datos masiva?**

Los dispositivos de migración de datos masiva utilizan un sistema de archivos ZFS con compresión LZ4 y cifrado AES de 256 bits.

<hr/>

## **¿Cuánto cuesta utilizar la migración de datos masiva en Estados Unidos?**

En Estados Unidos se aplica una tarifa plana de 395 dólares por dispositivo. Este coste incluye la cuota 295 dólares por el dispositivo, 100 dólares por la entrega UPS Next Day Air y 10 días hábiles de uso en las instalaciones del cliente.

<hr/>

## **¿Cuánto cuesta el uso de {{site.data.keyword.cos_full_notm}}?**

La transferencia de datos a {{site.data.keyword.cloud_notm}} no supone ningún coste para el usuario. Sin embargo, se aplican las tarifas estándares para los datos que se almacenan en {{site.data.keyword.cos_full}} o en cualquier otro servicio de {{site.data.keyword.cloud_notm}}. Encontrará los precios de {{site.data.keyword.cos_full}} para la oferta en varias regiones estándar en el enlace siguiente: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

<hr/>

## **¿Se puede adquirir un dispositivo de migración de datos masiva de {{site.data.keyword.cloud_notm}}?**

Los dispositivos de migración de datos masiva de {{site.data.keyword.cloud_notm}} no están a la venta.
