---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# Preguntas más frecuentes
{: #faqs}

Preguntas frecuentes sobre {{site.data.keyword.mdms_full}}.
{: shortdesc}

## ¿Qué es {{site.data.keyword.mdms_full_notm}}?
{: #what-is-mdms}
{: faq}

{{site.data.keyword.mdms_full_notm}} es un servicio de transferencia de datos físicos que acelera el traslado seguro de terabytes a petabytes de datos en {{site.data.keyword.cloud_notm}} mediante dispositivos de almacenamiento robustos y portátiles de 120 TB de capacidad utilizable.

## ¿Cómo empiezo a utilizar {{site.data.keyword.mdms_short}}?
{: #how-to-use-mdms}
{: faq}

Utilice [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} para enviar la solicitud. Cuando dicha solicitud se haya aprobado y procesado, se preconfigura el siguiente o los siguientes dispositivos disponibles y se le envían de acuerdo con la información de red y de envío que haya especificado. 

## ¿Quién debe utilizar {{site.data.keyword.mdms_short}}?
{: #who-uses-mdms}
{: faq}

Desde centros de datos y oficinas a ubicaciones remotas como embarcaciones y plataformas petroleras, los dispositivos
{{site.data.keyword.mdms_short}} están equipados para funcionar casi en cualquier entorno. {{site.data.keyword.mdms_short}} supone también una gran alternativa si las opciones de transferencia de datos a través de la red tienen un coste prohibitivo, son lentas o no están disponibles.

## ¿Cuántos datos puedo transferir utilizando {{site.data.keyword.mdms_short}}?
{: #how-much-data}
{: faq}

No hay prácticamente ningún límite por lo que respecta a la cantidad de datos que se pueden transferir, tanto si son algunos terabytes como si son muchos petabytes. Cada dispositivo tiene hasta 120 TB de capacidad utilizable en RAID-6, pero se pueden utilizar varios dispositivos para acomodar cargas de trabajo más grandes. {{site.data.keyword.mdms_short}} ofrece también compresión en línea, que puede aumentar aún más la capacidad utilizable dependiendo de cuánto se pueda comprimir el conjunto de datos. El tamaño máximo de un solo objeto está limitado a 10 TB.


## ¿Cómo utilizo varios dispositivos para mover cargas de trabajo mayores que superen 120 TB?
{: #using-multiple-devices}
{: faq}

Se utilizan varios dispositivos en paralelo o en serie para mover todos los datos en una sola migración o bien se utiliza un único dispositivo en migraciones iterativas. Por ejemplo, se pueden transferir de 1 PB de datos utilizando nueve dispositivos en paralelo o bien utilizar un único dispositivo para hacer nueve migraciones distintas. Si utiliza varios dispositivos en paralelo, tenga en cuenta que la velocidad de ingestión será menor.

## ¿Cuánto tardan en transferirse mis datos?
{: #transfer-timeline}
{: faq}

Desde el momento en que un cliente envía una solicitud de {{site.data.keyword.mdms_short}} hasta el momento en que los datos son accesibles en su grupo de IBM Cloud Object Storage, pueden pasar tan solo unos días. El rendimiento de transferencia se puede ver afectado por muchos factores como la red, el ancho de banda o el número de archivos que se transfieren. Por ejemplo, la transferencia de millones de archivos pequeños no tardará más que la misma cantidad de datos contenida en relativamente menos archivos de mayor tamaño.

## ¿Durante cuánto tiempo puedo tener un dispositivo {{site.data.keyword.mdms_short}}?
{: #device-onsite-time}
{: faq}

Un dispositivo puede guardarse en las instalaciones sin coste adicional durante los primeros 10 días laborables. Esto no incluye el día en que se envía el dispositivo ni el día en que se devuelve el dispositivo a IBM (máximo de 2 días). Si se necesita más tiempo para completar la ingestión, puede ampliar su uso por 30 dólares al día a partir de entonces. Se aplica a todas las regiones.

## ¿Qué interfaces de red admite {{site.data.keyword.mdms_short}}?
{: #supported-network-interfaces}
{: faq}

Los dispositivos {{site.data.keyword.mdms_short}} tienen interfaces de red de 10 Gbps con puertos de red de cobre SFP+ y RJ45 (CAT6a).

Los convertidores de RJ45 a SFP+ solo se incluyen con modelos de dispositivo que carecen de conexiones nativas SFP+. No se admite fibra en estos momentos.

## ¿Qué es la opción de envío predeterminado de {{site.data.keyword.mdms_short}}?
{: #shipping-options}
{: faq}

{{site.data.keyword.mdms_short}} utiliza la entrega de envío y devolución UPS Next Day Air para enviar todos los dispositivos. El coste se incluye en la tarifa baja y plana de 395 dólares por dispositivo. Por ahora, los clientes no pueden seleccionar otro método de envío.


## ¿En qué regiones está disponible {{site.data.keyword.mdms_short}}?
{: #regions-available}
{: faq}

{{site.data.keyword.mdms_short}} está disponible actualmente en los Estados Unidos (EE.UU.), la Unión Europea (UE), Japón, Australia, Brasil, Singapur, Hong Kong, Noruega, Corea del Sur, Canadá y México. Está en marcha una expansión geográfica adicional. El pedido en línea está disponible en la mayoría de las regiones. Para una región que no tenga pedido en línea, póngase en contacto con el representante de ventas de IBM para obtener ayuda sobre el uso del servicio.

Los dispositivos no se pueden enviar a través de fronteras internacionales (por ejemplo, no se puede solicitar un dispositivo en una región y enviarse a otra región), con la excepción de la Unión Europea y sus 28 países miembros.
{: note}

## ¿Cuál es la opción de envío predeterminado de {{site.data.keyword.mdms_short}} en EE.UU.?
{: #default-shipping-us}
{: faq}

{{site.data.keyword.mdms_short}} utiliza envíos nocturnos de UPS de ida y vuelta para los dispositivos en EE.UU. El coste del envío está incluido en el precio. Por ahora, los clientes no pueden seleccionar otro método de envío. 

## ¿Cuál es la opción de envío predeterminado de {{site.data.keyword.mdms_short}} en la UE?
{: #default-shipping-eu}
{: faq}

{{site.data.keyword.mdms_short}} utiliza envíos nocturnos de FedEx de ida y vuelta para los dispositivos en la Unión Europea. El coste del envío está incluido en el precio. Por ahora, los clientes no pueden seleccionar otro método de envío. 

## ¿Cuál es la opción de envío predeterminado de {{site.data.keyword.mdms_short}} en las demás regiones con soporte?
{: #default-shipping-other}
{: faq}

Para todas las regiones con soporte fuera de EE.UU. y la UE, los proveedores de envío y los tiempos de respuesta de envío varían. El coste del envío está incluido en el precio. Por ahora, los clientes no pueden seleccionar otro método de envío.

En estas regiones, IBM no puede reservar el envío de ida y vuelta en el momento en que se realiza el pedido. En su lugar, se reservan envíos de una sola dirección en el momento en que se necesita un envío. Para envíos de salida, deje un margen de al menos tres días laborables para que IBM pueda coordinar el envío de su dispositivo {{site.data.keyword.mdms_short}} después de que realice su solicitud.
{: note}

Para pedidos que no se realicen en EE.UU. ni en la Unión Europea, solicite un envío de devolución para el dispositivo al menos tres días laborables antes de la fecha en que desea enviar el dispositivo. Por ejemplo, si desea enviar el dispositivo el viernes, coordine un envío de devolución el lunes de esa misma semana. Puede solicitar en envío de devolución desde el separador
_Detalles de la solicitud_ del panel de control de {{site.data.keyword.mdms_short}}.
{: important}

## Estoy en Japón, Australia, Brasil, Canadá, México, Hong Kong, Singapur, Noruega o Corea del Sur. ¿Cómo solicito el envío de devolución de mi dispositivo {{site.data.keyword.mdms_short}}?
{: #shipping-timetable-other}
{: faq}

Si utiliza {{site.data.keyword.mdms_short}} fuera de las regiones de EE.UU. y la UE, necesita solicitar un envío de devolución para el dispositivo al menos tres días laborables antes de la fecha en que desea enviar el dispositivo. Por ejemplo, si desea enviar el dispositivo el viernes, coordine un envío de devolución el lunes de esa misma semana.

## ¿Cuánto cuesta importar datos en {{site.data.keyword.cloud_notm}}?
{: #data-transfer-cost}
{: faq}

No se aplica ningún cargo por transferir datos a {{site.data.keyword.cloud_notm}}.


## ¿Puedo utilizar {{site.data.keyword.mdms_short}} para exportar datos fuera de {{site.data.keyword.cloud_notm}}?
{: #exporting-data}
{: faq}

{{site.data.keyword.mdms_short}} no admite la exportación de datos fuera de {{site.data.keyword.cloud_notm}} en este momento.


## ¿{{site.data.keyword.mdms_short}} cifra mis datos?
{: #encryption}
{: faq}

{{site.data.keyword.mdms_short}} cifra todos los datos con el cifrado AES de 256 bits y proporciona una contraseña fuerte para desbloquear la agrupación de almacenamiento. Todas las transferencias de datos de {{site.data.keyword.IBM}} se realizan por SSL.

## ¿De qué manera {{site.data.keyword.mdms_short}} protege físicamente los datos?
{: #security}
{: faq}

Todos los dispositivos {{site.data.keyword.mdms_short}} se alojan en compartimentos robustos y duraderos. Los compartimentos son impermeables, a prueba de golpes y con detección de manipulaciones para garantizar el envío y la devolución del dispositivo, así como la seguridad de los datos.

## ¿Cómo realizo el seguimiento de mi solicitud durante el proceso de migración?
{: #how-to-track-request}
{: faq}

Para realizar un seguimiento del estado de su solicitud, vaya al separador _Detalles de la solicitud_ del panel de control de
{{site.data.keyword.mdms_short}} en la consola de {{site.data.keyword.cloud_notm}}.

## ¿Cómo borro mis datos del dispositivo {{site.data.keyword.mdms_short}} después de que se descarguen en {{site.data.keyword.cos_full_notm}}?
{: #data-erasure}
{: faq}

Tan pronto como se haya completado la descarga de sus datos en IBM Cloud Object Storage, IBM borrará inmediatamente el dispositivo utilizando los estándares de limpieza de datos NIST para garantizar el borrado completo de todos los datos del cliente de los dispositivos.

## ¿Cuáles son las interfaces de archivos en {{site.data.keyword.mdms_short}}?
{: #file-interfaces}
{: faq}

{{site.data.keyword.mdms_short}} admite los protocolos Network File System (NFS) y Server Message Block (SMB).

## ¿Cómo utilizo la interfaz de archivos en {{site.data.keyword.mdms_short}}?
{: #how-to-use-file-interface}
{: faq}

En primer lugar, desbloquee la agrupación de cifrado. A continuación, monte el recurso compartido en el servidor que contiene los datos que desea migrar. Empiece a copiar los archivos de datos en el recurso compartido de red.

## ¿Qué ventajas tiene la interfaz de archivos de {{site.data.keyword.mdms_short}}?
{: #file-interface-benefits}
{: faq}

La interfaz de archivos se basa en un archivo maduro y software de red que permite copiar y mover un gran número de archivos grandes a {{site.data.keyword.cloud_notm}}.

## ¿Cómo se almacenan los archivos en el dispositivo {{site.data.keyword.mdms_short}}?
{: #file-storage}
{: faq}

Los dispositivos {{site.data.keyword.mdms_short}} utilizan un sistema de archivos ZFS con compresión LZ4 y cifrado AES de 256 bits.

## ¿Cuánto cuesta utilizar {{site.data.keyword.mdms_short}} en Estados Unidos?
{: #pricing-us}
{: faq}

En EE.UU., se carga una tarifa plana de 395 dólares por dispositivo, incluyendo la fianza de dispositivo de 295 dólares, 100 dólares de envío nocturno de UPS de ida y vuelta y 10 días laborables de uso en sus instalaciones.

Los 10 días de uso in situ no incluyen el día en que se envía el dispositivo ni el día en que se devuelve el dispositivo a IBM (máximo de dos días). Si se necesita más tiempo para completar la migración más allá de los 10 días laborables permitidos, se le cobrará una tarifa de extensión de 30 dólares al día por cada día de uso adicional.

## ¿Cuánto cuesta utilizar {{site.data.keyword.mdms_short}} en la Unión Europea?
{: #pricing-eu}
{: faq}

En la UE, se carga una tarifa plana de 445 dólares por dispositivo, incluyendo la fianza de dispositivo de 295 dólares, 150 dólares de envío nocturno de FedEx de ida y vuelta y 10 días laborables de uso en sus instalaciones.

Los 10 días de uso in situ no incluyen el día en que se envía el dispositivo ni el día en que se devuelve el dispositivo a IBM (máximo de 2 días). Si se necesita más tiempo para completar la migración más allá de los 10 días permitidos, se le cobrará una tarifa de extensión de 30 dólares al día por cada día de uso adicional.

## ¿Cuánto cuesta utilizar {{site.data.keyword.mdms_short}} en todas las demás regiones con soporte?
{: #pricing-other}
{: faq}

En todas las demás regiones (Japón, Australia, Brasil, Canadá, México, Hong Kong, Singapur, Noruega y Corea del Sur), se carga una tarifa plana de 1145 dólares por dispositivo, incluyendo la fianza de dispositivo de 295 dólares, el envío de ida y vuelva de 850 dólares y 10 días laborables de uso en sus instalaciones.

Los 10 días de uso in situ no incluyen el día en que se envía el dispositivo ni el día en que se devuelve el dispositivo a IBM (máximo de 2 días). Si se necesita más tiempo para completar la migración más allá de los 10 días permitidos, se le cobrará una tarifa de extensión de 30 dólares al día por cada día de uso adicional.

Existen requisitos de envío especiales para estas regiones. Mire más arriba para ver más información.
{: note}

## ¿Se me cobrará el uso de {{site.data.keyword.cos_full_notm}}?
{: #pricing-cos}
{: faq}

La transferencia de datos en {{site.data.keyword.cloud_notm}} se produce sin coste alguno para usted. Sin embargo, se aplican las tarifas estándares para los datos que se almacenan en {{site.data.keyword.cos_full_notm}} o en cualquier otro servicio de {{site.data.keyword.cloud_notm}}. Para obtener más información sobre las opciones de precios de Cloud Object Storage, consulte [Tarifas de {{site.data.keyword.cos_full_notm}}](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}. 

## ¿Puedo comprar un dispositivo {{site.data.keyword.mdms_full_notm}}?
{: #purchasing-devices}
{: faq}

Los dispositivos {{site.data.keyword.mdms_full_notm}} no están disponibles para su compra.

## ¿Cómo mantiene el proceso de {{site.data.keyword.mdms_short}} la exclusividad de los nombres de objeto?
{: #object-name-uniqueness}
{: faq}

Para garantizar que los nombres de objetos son exclusivos cuando se copian en un grupo de Cloud Object Storage, se incluye un prefijo en el nombre de objeto de la vía de acceso. Por ejemplo, `/root/user/config.ini` se convierte en `root/user/config.ini` cuando se copia en el grupo.

## ¿Qué ocurre si el grupo de destino no existe en la cuenta de {{site.data.keyword.cos_full_notm}}?
{: #target-buckets}
{: faq}

Si el grupo de destino no existe, se crea. Si existe, debe estar vacío; de lo contrario la copia no puede continuar.  

## ¿Se omiten los enlaces durante el proceso de exploración?
{: #links-scan-process}
{: faq}

Sí. Los enlaces simbólicos y los enlaces fijos se omiten durante el proceso de exploración.
