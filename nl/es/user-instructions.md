---

copyright:
  years: 2018
lastupdated: "2018-08-02"

---
{:new_window: target="_blank"}

# Importación de datos al dispositivo de migración masiva de IBM Cloud

El dispositivo de migración de datos masiva de {{site.data.keyword.cloud}} es un dispositivo de almacenamiento portátil que puede presentar recursos compartidos montables del sistema de archivos de red (NFS) o CFS (Content Federations Services) de FileNet. El dispositivo se gestionar mediante una interfaz de navegador web. El dispositivo se envía al centro de datos, cargado con datos en el sitio y se devuelve a un centro de datos de {{site.data.keyword.BluSoftlayer_full}} y se carga en la cuenta de {{site.data.keyword.cos_full}}.


### Alimentación del dispositivo

El dispositivo se suministra con un cable de alimentación C13-US [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Si se utiliza el dispositivo fuera de Estados Unidos, es posible que sea necesario un adaptador de alimentación.

El dispositivo acepta todos los rangos de alimentación estándar. ![Rango de alimentación](/images/PowerRating.png)

**Nota:** para encender el dispositivo, debe encender el interruptor Mains mediante el conector.

![Interruptor Mains](/images/MDMSPowerOnOff.png)

Utilice el botón de encendido y apagado del sistema que hay a la derecha de los LED de enlace de conexión.

![Apagado y encendido del sistema](/images/MDMSSystemOnOff.png)

El dispositivo está encendido cuando se muestra el ID del sistema en la pantalla de LED.


### Configuración de la conectividad Ethernet

Debe establecer dos conexiones ethernet. Una conexión para la gestión de dispositivos mediante un navegador y la otra para el traslado de datos en la misma subred en la que residen los datos de origen.
{{site.data.keyword.cloud}} ofrece dos modelos de dispositivo MDMS. Un modelo solo da soporte a la conectividad RJ45. El otro modelo da soporte a cobre SFP+ y a RJ45. En función del modelo de dispositivo MDMS, siga las instrucciones correspondientes.


#### Configuración solo de RJ45

![RJ45](/images/RJ45PortZoom.png)

Los puertos se originan en el mismo dispositivo que los cables RJ45, y se suministran los cables CAT6A. Se proporcionan los adaptadores de cobre SFP+ para realizar las conversiones desde RJ45. Los adaptadores funcionan con todos los fabricantes de interruptores. Dichos adaptadores están ubicados en un bolsillo de la parte inferior de la tapa del contenedor de envío.

- Eth1 (1 GbE-B) se suele utilizar para la gestión de dispositivos y, por lo tanto, debe tener una pasarela especificada en la configuración de direcciones IP. Esto puede verse en la pantalla LCD después de que el dispositivo se encienda (véase la sección de configuración de direcciones IP). Este puerto se utiliza para que la interfaz de usuario basada en web esté disponible fuera de la subred de datos.

- Eth3 (10 GbE-B) se utiliza para la transferencia de datos y también se puede utilizar para la gestión del dispositivo. Esta conexión debe estar en la misma subred que los datos de origen o conectarse directamente al servidor si es necesario.


#### Configuración de cobre SFP+ y de RJ45

![Cobre SFP+](/images/sfp-ports-sized-port5.png)

Los puertos se originan en el mismo dispositivo que cobre SFP+ y RJ45. Se suministra tanto el cable CAT6A como el cable cobre SFP+.

- Eth5 10 GbE (5) se suele utilizar para la transferencia de datos, pero también se puede utilizar para la gestión del dispositivo. Este puerto solo se ejecuta a 10 GbE.

- Eth2 10 GbE (2) se suele utilizar para la gestión del dispositivo, pero también se puede utilizar para la transferencia de datos. Este puerto se puede ejecutar a una velocidad de 1 GbE o de 10 GbE. 


La conexión de transferencia de datos debe estar en la misma subred que los datos de origen o conectarse directamente al servidor.

Los valores de IP se pueden ver y gestionar desde la pantalla LCD después de que el dispositivo se encienda (véase la sección de configuración de direcciones IP).

>*Nota** - NO es necesario configurar ni utilizar ambos puertos si se puede acceder a uno de ellos a través de un navegador web.


## Carga de los datos

1.	El dispositivo se suministra preconfigurado con su dirección IP, nombre de usuario, agrupación de almacenamiento bloqueado y recurso compartido NFS. La contraseña de usuario y la contraseña de agrupación de almacenamiento se comunicarán en otro correo electrónico.

2.	Determine el lugar más adecuado para colocar el dispositivo. Debe estar al alcance del cable de alimentación y del cable de ethernet y en un lugar poco transitado.

3.	Coloque el dispositivo para conectarlo. No es necesario que el dispositivo se extraiga del compartimento portátil. Puede permanecer en el maletín de transporte mientras se utiliza. Asegúrese de que el dispositivo esté a temperatura ambiente y de que no haya condensación en el mismo. Conecte el dispositivo a la corriente mediante el cable de alimentación proporcionado debajo de la tapa del compartimento y enciéndalo.<br/>
    **Nota**: observe que hay dos interruptores de alimentación. ![Interruptores de alimentación](/images/MDMSPowerSwitch.png) 

4. Conecte el dispositivo a la red.
    - Conexión de RJ45 
  	  1. Extraiga el cable CAT6A de la tapa del compartimento y conéctelo al puerto Eth3 (10 GbE-B) que se muestra en la imagen.
![Puertos del dispositivo MDMS](/images/MDMSNewEth1and3.png)
      
      2. Conecte el adaptador de CAT6A a SFP proporcionado y conecte el conmutador de 10 Gb.
      3. Si se puede acceder a la dirección IP configurada para Eth3 con el navegador mediante `HTTPS://'Su-dirección-Eth3'`, continúe con el paso siguiente. De lo contrario, conecte el puerto Eth1 (1 GbE-B).<br/>
         >**Nota**: si tiene que modificar los valores de IP para Eth3 o Eth1, consulte la sección sobre configuración de direcciones IP.
    - Conexión de cobre SFP+
      1. Extraiga el cable de cobre SFP+ de la tapa del compartimento y conéctelo a Eth5 10 GbE (5)
         ![Puertos del dispositivo MDMS](/images/sfp-ports-sized-ports-labeled.png)
      2. Conecte el cable de cobre SFP+ al conmutador 10 Gb.
      3. Si se puede llegar a la dirección IP configurada para Eth5 mediante el navegador `HTTPS://'Su-dirección-Eth5'`, continúe con el siguiente paso; de lo contrario, conecte el puerto Eth2 (10/1 GbE-B).<br/>
         >**Nota**: si tiene que modificar los valores de IP para Eth5 o Eth2, consulte la sección sobre configuración de direcciones IP.


5. Abra el navegador y escriba `HTTPS://Su-dirección-Eth1`. Sustituya `Su-dirección-Eth1` por el valor de Eth1 correspondiente a su configuración de red. Acepte la excepción de certificado.

6. Utilice el nombre de usuario y la contraseña proporcionados para iniciar la sesión.<br/>
    ![Página de inicio de sesión](/images/Login.png)

7. El asistente de flujo presenta el acceso a los temas específicos utilizados habitualmente ordenados de izquierda a derecha.<br/>
    ![Iconos de flujo de trabajos](/images/workflow.png) <br/>
    >**NOTA**: el flujo de trabajo se puede reabrir con el **Gestor de trabajo** de la parte superior izquierda de la interfaz.

8.	Active la agrupación de almacenamiento preconfigurado.
    - Pulse **Desbloquear e iniciar agrupación de almacenamiento**.
    - Escriba la contraseña de la agrupación de almacenamiento y pulse **Aceptar**.      ![Activar agrupación de almacenamiento](/images/UnlockPool.png)

9. De forma predeterminada, el recurso compartido tiene habilitados los protocolos NFS y SMB sin restricciones de acceso. Para restringir el acceso a este recurso compartido (para NFS o SMB), pulse con el botón derecho del ratón el nombre del recurso compartido y seleccione el elemento de menú correspondiente.<br/>
   ![Restringir el acceso al recurso compartido](/images/ShareControls.png)

10. Cuando la agrupación de almacenamiento esté habilitada, el recurso compartido NFS está disponible para montar. En el flujo de trabajo, pulse **Ver recursos compartidos de red** para ver la vista de recursos compartidos de red. Cierre el flujo de trabajo, pulse con el botón derecho del ratón el recurso compartido y seleccione el mandato de montaje para ver el nombre del recurso compartido y la información de montaje. Monte el recurso compartido en el servidor de origen. Asegúrese de especificar la dirección IP del enlace de 10 GB.
![Montaje del recurso compartido](/images/MountCommand.png)

11. Copie los datos en el recurso compartido NFS. En el flujo de trabajo, pulse **Ver actividad de red** para mostrar la carga de entrada de Ethernet a medida que se transfieren datos al dispositivo en el enlace de 10 GB.
    ![Ver actividad](/images/UserGuide13.png)

12. En el flujo de trabajo, pulse **Ver agrupación de almacenamiento** para supervisar el uso de almacenamiento en el dispositivo.
    ![Ver agrupación de almacenamiento](/images/UserGuide14.png)

13.	Cuando la carga se complete, apague correctamente el sistema. En el flujo de trabajo, pulse **Cerrar dispositivo...**.![Cierre del dispositivo](/images/Shutdown.png)

14.	Desconecte el dispositivo, devuelva el cable de alimentación, el cable Ethernet y el adaptador de SFP+ en sus respectivas ubicaciones de almacenamiento debajo de la tapa.

16.	Adjunte la etiqueta de envío, avise al transportista y devuelva el dispositivo al centro de datos.


## Configuración de direcciones IP

La pantalla LCD del dispositivo se puede utilizar para configurar las direcciones IP de los puertos Ethernet. Mueva el cursor por el panel LCD mediante los botones **Arriba**, **Abajo**, **Atrás/ESC** y **Adelante/INTRO**. Con el botón **Intro** se accede a un menú y con el botón **Salir**, se sale de él.

Cuando edita una dirección IP o máscara de subred, el botón **Intro** hace avanzar un carácter cada vez; el botón **Salir** hace retroceder un paso cada vez. 

Los botones **Arriba** y **Abajo** permiten desplazarse por los números de la ubicación elegida.

Utilice **Salir** para volver al menú anterior.

Vaya a **Actualizar...** y pulse **Intro** para guardar la configuración.

  ![Pantalla LCD](/images/MDMSLCD.png)
