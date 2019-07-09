---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

keywords: set up bare metal server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configuración de un servidor nativo
{: #bm-set-up}

Puede configurar un servidor nativo como servidor dedicado.
{:shortdesc}

## Antes de empezar
* Navegue hasta el menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Configuración de un servidor nativo

Efectúe los pasos siguientes para configurar un servidor nativo:

1. En el menú, pulse **Dispositivos** > **Lista de dispositivos** y busque su sistema. Todos los dispositivos están detallados en la lista de dispositivos, donde puede gestionar dispositivos, actualizar dispositivos o generar gráficos de uso de ancho de banda.

2. Gestione el servidor de una de las siguientes formas:
  * Pulse la flecha junto a Nombre de dispositivo para ver un resumen y gestionar los dispositivos desde la vista Instantánea.
  * Pulse el Nombre de dispositivo del servidor para ver una lista detallada y gestionar los dispositivos desde la pantalla Detalles de dispositivo.

3. Registre la dirección IP y las credenciales en un lugar seguro, de forma que pueda acceder a la información rápidamente sin tener que iniciar sesión en el Portal de clientes cada vez que la necesite. Puede registrar esta información de un solo dispositivo o de todos los dispositivos asociados a su cuenta:
  * Consulte las IP de dispositivos individuales en la Lista de dispositivos.
  * Consulte las contraseñas raíz de dispositivos individuales en la vista Instantánea del dispositivo.
  * Puede visualizar las IP de varios dispositivos utilizando la opción **Descargar CSV** del menú **Lista de dispositivos**. A continuación, seleccione **Descargar CSV** en la rueda dentada de **Configuración** para descargar una lista completa de dispositivos y detalles en formato de hoja de cálculo.

4. Actualice las credenciales para los sistemas operativos y otro software. Todo el software que se carga en el dispositivo durante el proceso de suministro lleva asignadas unas credenciales temporales. Puede ver y gestionar estas credenciales en el separador Contraseñas de cada dispositivo en el Portal de clientes. Utilice estas credenciales temporales para acceder al software por primera vez. A continuación, cambie la contraseña del software siguiendo las indicaciones para contraseñas fuertes. Cree una contraseña que consista en una combinación de letras, números y símbolos. Opcionalmente, puede almacenar actualizaciones de contraseña en el separador Contraseñas para cada dispositivo. Sin embargo, cuando almacena contraseñas en el portal de clientes, cualquier persona con acceso a la cuenta y con permisos apropiados puede ver las contraseñas que hay almacenadas en la pantalla Contraseñas.

5. Acceda al servidor en la red privada. Puede utilizar la red privada de infraestructura de {{site.data.keyword.cloud_notm}} para interactuar con los dispositivos mediante RDP (remote desktop, escritorio remoto) utilizando SSH y KVM sobre IP. Puede utilizar la herramienta Acceso de VPN para establecer una conexión de red privada al punto final de VPN con SSL más cercano o al punto final que prefiera. El acceso de VPN también es necesario para interactuar con varios servicios. Para acceder a la red privada, edite el acceso VPN del usuario desde la Lista de usuarios. Para acceder a la Lista de usuarios, pulse **Cuenta** > **Usuarios** > **Lista de usuarios**. Utilice la página [Red privada virtual ![Icono de enlace externo](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} para conectarse a una de las distintas opciones de VPN.

6. Defina una supervisión para comprobar el estado del servidor y saber así cuándo escalar. Puede utilizar servicios de supervisión estándar o Nimsoft. Puede utilizar la supervisión estándar, o básica, con el método de ping y respuesta mediante el uso de un ping lento o de servicio desde el portal de clientes. También puede utilizar supervisión Nimsoft, o avanzada, desde el portal de clientes o en 1 de estos 3 niveles: básico, avanzado y premium.

7. Proteja el sistema. Utilice los cortafuegos de hardware disponibles para proteger el dispositivo. Puede suministrar cortafuegos de hardware a petición sin tiempo de inactividad, si las reglas están establecidas correctamente, para proteger el servidor ante actividad no deseada. Una vez que solicite el cortafuegos, debe habilitarlo y definir reglas.

8. Planifique copias de seguridad para asegurarse de que los datos se almacenen de forma segura fuera del dispositivo y poder volver a cargar los datos en caso de que se pierdan. Puede elegir entre diversos servicios de copia de seguridad para almacenar los datos en una ubicación segura:
  * IBM Cloud Backup es un sistema de copia de seguridad automático basado en agente. IBM Cloud Backup es una solución automatizada de muy fácil activación (“set-and-forget”) para gestionar su dispositivo. Es compatible con el software de Microsoft, como por ejemplo Exchange y SQL a través de plug-ins adicionales. Los usuarios de IBM Cloud Backup interactúan con este servicio a través de la aplicación basada en web WebCC de IBM Cloud Backup.
  * R1Soft Continuous Data Protection (CDP) se puede instalar en el servidor o en una máquina virtual autogestionada. Se recomienda utilizarlo si busca una sola interfaz para gestionar todas sus copias de seguridad. Puede interactuar con R1Soft CDP a través de su propio sistema de gestión, lo que permite instalar agentes en máquinas virtuales y ofrece plugins de base de datos para obtener funcionalidad extra.
