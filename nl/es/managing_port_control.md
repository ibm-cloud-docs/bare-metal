---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gestión del control de puerto para un dispositivo
{: #bm-manage-port-control}

Cada dispositivo asociado con una cuenta tiene dos puertos de red que reciben tráfico entrante, uno para el tráfico de red pública y otro para el tráfico de red privada. Puede habilitar o inhabilitar estos puertos en cualquier momento para controlar el tráfico de red que recibe un dispositivo. Siga los pasos siguientes para actualizar los valores de control de puerto para un dispositivo.

## Antes de empezar
* Navegue hasta el menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Gestionar el control de puerto para un dispositivo

1. Acceda a la **Lista de dispositivos** y seleccione el **Nombre de dispositivo** que desea actualizar.  
2. Pulse la lista desplegable **Acciones** correspondiente al dispositivo.
3. Seleccione **Control de puerto**.
4. Actualice los recuadros desplegables *Red pública* y/o *Red privada* realizando una de las acciones siguientes:
   * Seleccione la velocidad deseada para habilitar el acceso de red.
   * Seleccione Desconectado para inhabilitar el acceso de red.
5. Pulse el botón Actualizar.
6. Pulse el botón Cerrar para cerrar la ventana.

## Pasos siguientes

Si ha seleccionado **Inhabilitado**, el acceso de red para el puerto inhabilitado cesará para la interfaz de dispositivo. Si ha seleccionado **Habilitado**, el acceso de red estará disponible para el puerto habilitado. El control de puerto permanece en el valor seleccionado hasta que se haya modificado manualmente.
