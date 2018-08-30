---

copyright:

  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configuración de un servidor nativo
{: #customerportal_setupbaremetal}

Puede configurar un servidor nativo como servidor dedicado.
{:shortdesc}

Efectúe los pasos siguientes para configurar un servidor nativo:

1. Inicie sesión en el portal de clientes de {{site.data.keyword.BluSoftlayer_full}} con sus credenciales exclusivas.

2. En el menú, pulse **Dispositivos** > **Lista de dispositivos** y busque su sistema. Todos los dispositivos están detallados en la lista de dispositivos, donde puede gestionar dispositivos, actualizar dispositivos o generar gráficos de uso de ancho de banda.

3. Gestione el servidor de una de las siguientes formas:
  * Pulse la flecha situada junto al Nombre de dispositivo para ver un resumen y gestionar los dispositivos desde la vista Instantánea.
  * Pulse el Nombre de dispositivo del servidor para ver una lista detallada y gestionar los dispositivos desde la pantalla Detalles de dispositivo.

4. Registre la dirección IP y las credenciales en un lugar seguro, de forma que pueda acceder a la información rápidamente sin tener que iniciar sesión en el Portal de clientes cada vez que la necesite. Puede registrar esta información de un solo dispositivo o de todos los dispositivos asociados a su cuenta:
  * Consulte las IP de dispositivos individuales en la Lista de dispositivos.
  * Consulte las contraseñas raíz de dispositivos individuales en la vista Instantánea del dispositivo.
  * Consulte las IP de varios dispositivos con la opción **Descargar CSV** del menú **Lista de dispositivos**. A continuación, seleccione **Descargar CSV** en la rueda dentada de **Configuración** para descargar una lista completa de dispositivos y detalles en formato de hoja de cálculo.

5. Actualice las credenciales para los sistemas operativos y otro software. Todo el software que se carga en el dispositivo durante el proceso de suministro lleva asignadas unas credenciales temporales. Puede ver y gestionar estas credenciales en el separador Contraseñas de cada dispositivo en el Portal de clientes. Utilice estas credenciales temporales para acceder al software la primera vez y luego cambie la contraseña del software por una contraseña segura que esté compuesta por una combinación de letras, números y símbolos. Opcionalmente, puede almacenar las actualizaciones de contraseña en el separador Contraseñas de cada dispositivo; sin embargo, cuando almacena contraseñas en el portal de clientes, cualquier persona con acceso a la cuenta y con permisos apropiados puede ver las contraseñas que hay almacenadas en la pantalla Contraseñas.

6. Acceda al servidor en la red privada. Puede utilizar la red privada de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} para interactuar con los dispositivos mediante RDP (remote desktop, escritorio remoto) con SSH y KVM sobre IP. Puede utilizar la herramienta Acceso de VPN para establecer una conexión de red privada al punto final de VPN con SSL más cercano o al punto final que prefiera. El acceso de VPN también es necesario para interactuar con varios servicios. Para acceder a la red privada, edite el acceso VPN del usuario desde la Lista de usuarios. Para acceder a la Lista de usuarios, pulse **Cuenta** > **Usuarios** > **Lista de usuarios**. Utilice la página [Red privada virtual ![Icono de enlace externo](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} para conectarse a una de las distintas opciones de VPN.

7. Defina una supervisión para comprobar el estado del servidor y saber así cuándo escalar. Puede utilizar servicios de supervisión estándar o Nimsoft. Puede utilizar la supervisión estándar, o básica, con el método de ping y respuesta mediante el uso de un ping lento o de servicio desde el portal de clientes. También puede utilizar supervisión Nimsoft, o avanzada, desde el portal de clientes o en uno de estos tres niveles: básico, avanzado y premium.

8. Proteja el sistema. Utilice los cortafuegos de hardware disponibles para asegurarse de que el dispositivo esté protegido en todo momento. Puede suministrar cortafuegos de hardware a petición sin tiempo de inactividad, si las reglas están establecidas correctamente, para proteger el servidor ante actividad no deseada. Una vez que solicite el cortafuegos, debe habilitarlo y definir reglas.

9. Planifique copias de seguridad para asegurarse de que los datos se almacenen de forma segura fuera del dispositivo y pueda cargarlos de nuevo si el dispositivo se pierde. Puede elegir diversos servicios de copia de seguridad para almacenar los datos en una ubicación segura:
  * La copia de seguridad de EVault es un sistema de copia de seguridad automático basado en agente. Se trata de una conocida solución automatizada de muy fácil activación (“set-and-forget”) para la gestión del dispositivo. Es compatible con el software de Microsoft, incluido Exchange y SQL a través de conectores adicionales. Los usuarios de EVault interactúan con este servicio a través de la aplicación basada en web WebCC de EVault.
  * R1Soft Continuous Data Protection (CDP) se puede instalar en el servidor o en una máquina virtual autogestionada. Se recomienda utilizarlo si busca una sola interfaz para gestionar todas sus copias de seguridad. Puede interactuar con R1Soft CDP a través de su propio sistema de gestión, lo que permite instalar agentes en máquinas virtuales y ofrece plugins de base de datos para obtener funcionalidad adicional.
