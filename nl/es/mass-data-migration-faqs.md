---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Preguntas frecuentes sobre la migración de datos masiva de {{site.data.keyword.cloud_notm}}

## Pregunta 1. ¿Qué es la {{site.data.keyword.cloud_notm}} migración de datos masiva? 
La migración de datos masiva de {{site.data.keyword.cloud}} es un servicio de transferencia de datos físicos que acelera el traslado seguro de terabytes a petabytes de datos en {{site.data.keyword.cloud_notm}} mediante dispositivos de almacenamiento robustos y portátiles de 120 TB de capacidad utilizable. 

## Pregunta 2. ¿Cómo se empieza a utilizar la migración de datos masiva? 
Utilice [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} para enviar la solicitud. Una vez que se apruebe y procese dicha solicitud, se preconfigurarán el próximo o próximos dispositivos disponibles y se le enviarán de acuerdo con la información de red y envío que proporcione. Utilice el enlace siguiente para empezar ahora: https://control.softlayer.com/storage/mdms

## Pregunta 3. ¿Quién debería utilizar la migración de datos masiva? 
Los dispositivos de migración de datos masiva están equipados para rendir en casi cualquier entorno: desde los centros de datos y oficinas hasta lugares remotos, almacenes y barcos. La migración de datos masiva también es una alternativa si las opciones por la red tienen un coste prohibitivo, son demasiado lentas o no están disponibles.  

## Pregunta 4. ¿Cuántos datos se pueden transferir con la migración de datos masiva?
No hay prácticamente ningún límite por lo que respecta a la cantidad de datos que se pueden transferir, tanto si son algunos terabytes como si son petabytes. Cada dispositivo tiene hasta 120 TB de capacidad utilizable en RAID-6, pero se pueden utilizar varios dispositivos para acomodar cargas de trabajo más grandes.

## Pregunta 5. ¿Cómo se pueden utilizar varios dispositivos para mover cargas de trabajo que superen los 120 TB? 
Se utilizan varios dispositivos en paralelo o en serie para mover todos los datos en una sola migración o bien se utiliza un único dispositivo en migraciones iterativas. Por ejemplo, se pueden transferir de 1 PB de datos utilizando 9 dispositivos en paralelo o bien utilizar un único dispositivo para hacer 9 migraciones distintas.

## Pregunta 6. ¿Cuánto tardan en transferirse los datos? 
Desde el momento en que un cliente envía una solicitud de migración de datos masiva hasta el momento en que sus datos son accesibles en su grupo de {{site.data.keyword.cos_full}}, pueden pasar tan solo 7 días.  

## Pregunta 7. ¿Durante cuánto tiempo se puede tener un dispositivo de migración de datos masiva?  
Un dispositivo puede estar en unas instalaciones sin coste alguno durante los primeros 10 días hábiles. Esto no incluye el día se envía el dispositivo ni el día que lo recibe. Si se necesita más tiempo para completar la ingesta, se puede prorrogar su uso por 30 dólares al día a partir del undécimo día (se aplica a EE. UU. y la UE). 

## Pregunta 8. ¿Qué interfaces de red admite la migración de datos masiva?  
Los dispositivos de migración de datos masiva tienen interfaces de red con 10 Gbps con conversor RJ45 (CAT6a) y cobre SFP+ incluido--puertos de red.

## Pregunta 9. ¿Qué es la opción de envío predeterminado de la migración de datos masiva? 
La migración de datos masiva utiliza la entrega de envío y devolución UPS Next Day Air para enviar todos los dispositivos. El coste se incluye en la tarifa baja y plana de 395 dólares por dispositivo. Por ahora, los clientes no pueden seleccionar otro método de envío.

## Pregunta 10. ¿En qué regiones está disponible la migración de datos masiva? 
Actualmente la migración de datos masiva solo está disponible en Estados Unidos y en la Unión Europea. Todos los datos se migran a {{site.data.keyword.cos_full}} en los niveles de servicio de varias regiones estándar de EE. UU. o de la UE. Los dispositivos no se pueden enviar desde una región y devolverse en otra.

## Pregunta 11: ¿Cuánto cuesta importar datos en el {{site.data.keyword.cloud_notm}}? 
No se aplica ningún cargo por transferir datos en el {{site.data.keyword.cloud_notm}}.

## Pregunta 12: ¿se puede utilizar la migración de datos masiva para exportar datos fuera de {{site.data.keyword.cloud_notm}}? 
Por ahora, la migración de datos masiva no admite la exportación de datos fuera del {{site.data.keyword.cloud_notm}}.

## Pregunta 13. ¿La migración de datos masiva cifra los datos? 
La migración masiva de datos cifran todos los datos con el cifrado AES de 256 bits y proporciona una contraseña fuerte para desbloquear la agrupación de almacenamiento. Todas las transferencias de datos de {{site.data.keyword.IBM}} se realizan por SSL.

## Pregunta 14. ¿Cómo protege físicamente los datos la migración de datos masiva? 
Todos los dispositivos de migración de datos masiva se alojan en compartimentos robustos y duraderos. Los compartimentos son impermeables, a prueba de golpes y con detección de manipulaciones para garantizar el envío y la devolución del dispositivo, así como la seguridad de los datos. 

## Pregunta 15. ¿Cómo se realiza el seguimiento de una solicitud durante el proceso de migración? 
Para realizar el seguimiento del estado de una solicitud, consulte el apartado de solicitudes activas en la página de migración de datos masiva de [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. También puede iniciar la sesión en el portal mediante el enlace siguiente: https://control.softlayer.com/storage/mdms

## Pregunta 16. ¿Cómo se borran los datos del dispositivo una vez que se descargan en {{site.data.keyword.cos_full_notm}}?
Una vez que se ha completado el traspaso de datos a {{site.data.keyword.cos_full}}, {{site.data.keyword.IBM}} inicia inmediatamente una limpieza de datos de nivel DOD para borrar los datos del dispositivo de forma permanente. 

## Pregunta 17: ¿Qué interfaz tiene la migración de datos masiva? 
La migración de datos masiva utiliza el sistema de archivos de red (NFS).

## Pregunta 18: ¿Cómo se utiliza la interfaz de archivos de la migración de datos masiva? 
Después de desbloquear la agrupación de cifrado, debe montarse el recurso compartido NFS en el servidor que contiene los datos que se vayan a migrar y, a continuación, empezar a copiar los archivos de datos en el recurso compartido NFS.

## Pregunta 19: ¿Qué ventajas tiene la interfaz de archivos de la migración de datos masiva? 
La interfaz de archivos se basa en un archivo maduro y software de red que permite copiar y mover un gran número de archivos grandes a {{site.data.keyword.cloud_notm}}.

## Pregunta 20: ¿Cómo se almacenan los archivos en el dispositivo de migración de datos masiva? 
Los dispositivos de migración de datos masiva utilizan un sistema de archivos ZFS con compresión LZ4 y cifrado AES de 256 bits.

## Pregunta 21. ¿Cuánto cuesta utilizar la migración de datos masiva en Estados Unidos? 
En Estados Unidos se aplica una tarifa plana de 395 dólares por dispositivo, que incluye la cuota 295 dólares por el dispositivo, 100 dólares por la entrega UPS Next Day Air y 10 días hábiles de uso en las instalaciones del cliente. 

## Pregunta 22. ¿Se paga el uso de {{site.data.keyword.cos_full_notm}} ? 
La transferencia de datos en la {{site.data.keyword.cloud_notm}} no supone ningún coste para el usuario. Sin embargo, se aplicarán tarifas estándar para los datos almacenados en {{site.data.keyword.cos_full}} o cualquier otro servicio de {{site.data.keyword.cloud_notm}}. Encontrará los precios de {{site.data.keyword.cos_full}} para la oferta en varias regiones estándar en el enlace siguiente: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## Pregunta 23. ¿Se puede comprar un dispositivo de migración de datos masiva de {{site.data.keyword.cloud_notm}}? 
Los dispositivos de migración de datos masiva de {{site.data.keyword.cloud_notm}} no se pueden comprar. 
