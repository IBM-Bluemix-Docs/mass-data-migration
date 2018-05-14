---

copyright:
  years: 2018
lastupdated: "2018-04-06"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Instrucciones del usuario

## Visión general

El dispositivo de migración de datos masiva de {{site.data.keyword.cloud}} es un dispositivo de almacenamiento portátil que puede presentar recursos compartidos NFS o CFS instalables y que se gestiona mediante una interfaz de navegador web.  El dispositivo se envía a las instalaciones de un cliente cargado con datos y se devuelve a un centro de datos de {{site.data.keyword.BluSoftlayer_full}} y se carga {{site.data.keyword.cos_full}} en la cuenta del cliente y un grupo.


### Alimentación

El dispositivo se envía con un cable de alimentación C13-US [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Si se utiliza el dispositivo fuera de Estados Unidos, es posible que sea necesario un adaptador de alimentación.

El dispositivo acepta todos los rangos de alimentación estándar. ![Rango de alimentación](/images/PowerRating.png)


### Conectividad Ethernet

Deben hacerse dos conexiones de Ethernet.  Uno para la gestión de dispositivos mediante un navegador y otra para el traslado de datos en la misma subred en la que residen los datos de origen.

Ambos puertos se originan en el mismo dispositivo que los cables RJ45, y se suministran los cables CAT6A.  Se proporcionan los adaptadores de cobre SFP+ para realizar las conversiones desde RJ45.  Se garantiza que los adaptadores pueden funcionar con todos los fabricantes de conmutadores. Dichos adaptadores están ubicados en un bolsillo de la parte inferior de la tapa de envío.

Eth1 (1GbE-B) se utiliza para la gestión de dispositivos y, por lo tanto, debería tener una pasarela especificada en la configuración de direcciones IP.  Esto puede verse mediante la pantalla LCD después de que el dispositivo se encienda (ver Anexo de configuración de direcciones IP a continuación).

Eth3 (10 GbE-B) se utiliza para la transferencia de datos.  Dicha conexión debería estar en la misma subred que los datos de origen o conectarse directamente al servidor si es necesario.

Si se requiere un factor de forma diferente de conexión Ethernet, el cliente debe proporcionar el conversor.



## Instrucciones paso a paso para el usuario

1.	El dispositivo llega preconfigurado con su dirección IP, nombre, agrupación de almacenamiento bloqueado y recurso compartido NFS.  La contraseña de usuario y la contraseña de agrupación de almacenamiento se comunicarán en otro correo electrónico.

2.	Determine el lugar más adecuado para colocar el dispositivo; donde lleguen tanto la alimentación como las conexiones Ethernet (1 GbE y 10 GbE) y donde pase poca gente.

3.	Coloque el dispositivo para conectarlo; puede permanecer en el maletín de transporte durante su uso. Asegúrese de que el dispositivo esté a temperatura ambiente y de que no haya condensación en él. Conecte el dispositivo a la corriente mediante el cable de alimentación proporcionado debajo de la tapa del compartimento y enciéndalo.<br/>
    **Nota**: hay dos interruptores de alimentación. ![Interruptores de alimentación](/images/MDMSPowerSwitch.png)
    **Nota**: no es necesario que el dispositivo se extraiga del compartimento portátil.

4.	Extraiga el cable CAT6A de la tapa del compartimento y conéctelo al puerto Eth3 (10 GbE-B) que se muestra en la imagen siguiente.     ![](/images/MDMSNewEth1and3.png)

5.	Conecte el adaptador de CAT6A a SFP proporcionado y conecte el conmutador de 10 Gb.

6.	Si se puede llegar a la dirección IP configurada para Eth3 mediante el navegador HTTPS: //'Dirección-Eth3', siga el próximo paso; de lo contrario, conecte el puerto Eth1 (1 GbE-B).<br/>
    **Nota**: consulte el anexo de configuración IP a continuación si tiene que modificar los valores de IP para Eth3 o Eth1.

7. Abra el navegador y especifique HTTPS: //'Dirección-Eth1'. Especifique Eth1 como adecuada para su configuración de red. Acepte la excepción de certificado.

8.	Utilice el nombre de usuario y la contraseña proporcionados para iniciar la sesión.<br/>
    ![Página de inicio de sesión](/images/Login.png)

9.  El asistente de flujo presenta el acceso a los temas específicos utilizados habitualmente ordenados de izquierda a derecha.  <br/>
    ![Iconos de flujo de trabajos](/images/workflow.png) <br/>
    **NOTA**: el flujo de trabajo se puede reabrir con el botón Gestor de trabajo de la parte superior izquierda de la GUI.

10.	Activar la agrupación de almacenamiento preconfigurado:
    - Haga clic en **Desbloquear e iniciar agrupación de almacenamiento**.
    - Escriba la contraseña de la agrupación de almacenamiento y pulse **Aceptar**.      ![Activar agrupación de almacenamiento](/images/UnlockPool.png)

11. De forma predeterminada, el recurso compartido tiene habilitados los protocolos NFS y SMB sin restricciones de acceso al recurso compartido. Para restringir el acceso a este recurso compartido (para NFS y/o SMB), pulse con el botón derecho del ratón el nombre del recurso compartido y seleccione el elemento de menú correspondiente.<br/>
    ![Restringir el acceso al recurso compartido](/images/ShareControls.png)

12. Una vez que la agrupación de almacenamiento esté habilitada, el recurso compartido NFS está disponible para montar.  En el flujo de trabajo, pulse **Ver recursos compartidos de red** para ver la vista de recursos compartidos de red.  Cierre el flujo de trabajo, pulse con el botón derecho del ratón el recurso compartido y seleccione el mandato de montaje para ver el nombre del recurso compartido y la información de montaje. Monte el recurso compartido en el servidor de origen y cargue los datos. Asegúrese de especificar la dirección IP del enlace de 10 Gb al montar el recurso compartido.
    ![Montaje del recurso compartido](/images/MountCommand.png)

13. Empiece a copiar los datos en el recurso compartido NFS. En el flujo de trabajo, pulse **Ver actividad de red** para mostrar la carga de entrada de Ethernet en la GUI a medida que se transfieren datos al dispositivo en el enlace de 10 Gb.
    ![Ver actividad](/images/UserGuide13.png)


14. En el flujo de trabajo, pulse **Ver agrupación de almacenamiento** para supervisar el uso de almacenamiento en el dispositivo.
    ![Ver agrupación de almacenamiento](/images/UserGuide14.png)


15.	Cuando la carga se complete, apague correctamente el sistema. En el flujo de trabajo, pulse **Cerrar dispositivo...**.  
    ![Cierre del dispositivo](/images/Shutdown.png)

16.	Desconecte el dispositivo, devuelva el cable de alimentación, el cable Ethernet y el adaptador de SFP+ en sus respectivas ubicaciones de almacenamiento debajo de la tapa.

17.	Adjunte siempre la etiqueta de envío, avise al expedidor y devuelva el dispositivo al centro de datos para cargarlo en Cloud Object Storage.


## Anexo de configuración de la dirección IP
El panel LCD de la parte superior del dispositivo se puede utilizar para configurar las direcciones IP de los puertos Ethernet.
Vaya al panel LCD utilizando los botones Arriba, Abajo, Atrás/ESC y Adelante/INTRO. Con el botón Intro se accede a un menú y con el botón Salir, se sale de él.

Al editar una dirección IP o máscara de subred, el botón Intro hace avanzar un carácter cada vez; el botón Salir hace retroceder un paso cada vez. Los botones Arriba y Abajo permiten desplazarse por los números de la ubicación elegida.
Utilice Salir atrás para volver al menú anterior.  

Vaya al elemento de menú “Actualizar...” y pulse Intro para guardar la configuración.

  ![](/images/MDMSLCD.png)
