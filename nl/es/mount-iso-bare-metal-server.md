---

copyright:
  years: 2017, 2019
lastupdated: "2018-06-03"

keywords: mount iso bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Montaje de una ISO en un servidor nativo
{: #bm-mount-iso}

## Visión general

Aunque la mayoría de los clientes de {{site.data.keyword.cloud}} utilizan uno de los sistemas operativos estándar incluidos con nuestros servidores, puede montar ISO (imágenes de disco) personalizadas en los servidores. Dispone de tres opciones para montar ISO personalizadas.

Para que los métodos funcionen, es necesario conectarse a la red privada a través del servicio VPN de SL, como por ejemplo [SoftLayer SSL VPN Portal - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login) o a través de otro servidor que esté conectado a la red.

**Nota:** Las imágenes de disco de hardware de Lenovo superiores a 50 MB deben montarse utilizando la interfaz de la consola IMM > separador soporte.

## Opción 1 (preferida): utilizar IPMI (ISO en una compartición de CIFS)
{: #bm-mount-iso-opt-1}

Si ya tiene una infraestructura desplegada en {{site.data.keyword.cloud_notm}}, puede configurar un servidor existente para ofrecer una compartición de CIFS a la red interna. A continuación, puede montar en un servidor nativo cualquier ISO que se encuentre allí.

Este es el método preferido para instalar un SO personalizado en un servidor nativo, porque se instala en la red local, que es muy rápida y puede mantener la ISO montada incluso si cierra la sesión o se desconecta de la interfaz de gestión.

Siga estos pasos para instalar un SO personalizado desde una compartición de CIFS:

1. Asegúrese de que ha colocado la ISO en la compartición de CIFS.
* Inicie sesión en la consola de gestión de IPMI apuntando su navegador web a la dirección IP especificada en cloud.ibm.com en dispositivos -> su servidor (detalles del dispositivo) -> Gestión remota. El nombre de usuario y la contraseña también se especifican aquí.
* Pase el ratón sobre **Virtual Media** y pulse **CD-ROM image**.
* Rellene la información apropiada y pulse **Save and Mount**.
* No todos los usuarios tienen permiso para cambiar el BIOS del servidor. Si es necesario, puede abrir una incidencia de soporte para solicitar:
  * Privilegios de administrador de usuario root en IPMI (para poder cambiar la modalidad de Virtual Media Attach)
  * Cambiar la secuencia de arranque a 'IPMI Virtual Disk' como primera opción de arranque.
* Una vez realizados estos cambios, vuelva a la consola de gestión de IPMI y vaya a Configuration -> Remote session y cambie la modalidad de Attach a **attach**. En algunas consolas anteriores de IPMI, puede saltarse esta opción.
* Rearranque el servidor y arranque desde el soporte virtual.


## Opción 2: utilizar IPMIView (ISO en una compartición de CIFS)
{: #bm-mount-iso-opt-2}

Requisitos previos:<br/>
* Tener una ISO arrancable
* Un servidor CIFS de Windows o almacenamiento NAS para almacenar la ISO arrancable
* Que la ISO esté cargada en el almacenamiento de archivos (NAS) asociado con el servidor.
* Que IPMIView esté instalado, o acceder a la consola de KVM
* Que el archivo ISO se pueda descargar con wget
* Tener acceso de SSH con privilegios para acceder o instalar paquetes y crear un montaje


### Linux y Windows
Siga estos pasos para montar una ISO con IPMIView.
1. Mediante una incidencia de soporte, solicite que el servidor arranque el CD-ROM virtual como primer dispositivo. Cada dispositivo se debe arrancar desde su CD-ROM virtual asociado. Puede revertir este valor después de instalar el SO.
* Establezca una conexión VPN a [VPN](http://www.softlayer.com/VPN-Access). Si utiliza Microsoft Internet Explorer, asegúrese de incluir .softlayer.com y .cloud.ibm.com en la lista de sitios de confianza y tener JAVA actualizado.
* Copie el soporte ISO en el NAS o en el servidor CIFS de Windows.
  * Conéctese a la jumpbox de Linux mediante SSH.
  * Monte la compartición de NAS en la jumpbox de Linux:

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * Monte la clave de parámetro de mandato:
        NAS_SERVER_NAME_ORIP = El nombre o IP del almacenamiento NAS.
        /SLN#####-2 = El nombre de usuario y el nombre de carpeta para conectarse al almacenamiento NAS.
        NAS_STORAGE_PW = La contraseña para el almacenamiento NAS.
        /mnt/nasmount = La carpeta para montar el almacenamiento NAS.
  * Cambie el directorio a la nueva carpeta de montaje de NAS.
        cd /mnt/nasmount
  * Descargue el archivo iso mediante wget.
        wget http://www.linktoyouriso.com/isofilename.iso
  Verá una confirmación de que la descarga se ha realizado correctamente.
* Descargue IPMIView de aquí:
      https://www.servethehome.com/download-supermicro-ipmiview-latest-version/
* Conéctese al servidor mediante la IP de gestión.<br>
      1. Conéctese a `winadmin`.
      2. Abra IPMIView y vaya a **Archivo > Nuevo > Sistema**.
      3. Utilice la dirección IP de IPMI desde el objeto de hardware para completar los campos Nombre de servidor y dirección IP.<br>
      4. Efectúe una doble pulsación en el sistema que tenga la misma dirección IP de la izquierda y especifique ADMIN para el ID de inicio de sesión y la contraseña de IPMI del objeto de hardware.
      5. Una vez conectado, tiene muchos separadores disponibles en la ventana. Puede utilizar la **Consola de texto** o **Consola de KVM** para conectarse al servidor.

* Abra el separador Virtual Media
* Indique los detalles de conexión de la imagen de CD-ROM.
  *
    * Share host = la dirección IP del almacenamiento NAS. Puede obtener este valor haciendo ping en el nombre de servidor de almacenamiento NAS. Por ejemplo, `ping nas501.service.softlayer.com`
    * Share Name = el nombre de usuario del almacenamiento NAS
    * Path to image = el nombre del archivo ISO, en el formato siguiente:
          \NASusername\isoname.iso (i.e. \SLN123456\centos6.iso)
    * User = el nombre de usuario del almacenamiento NAS
    * Password = la contraseña del almacenamiento NAS
* Rearranque el servidor
* Abra la vista de la consola de KVM
* Siga los indicadores del sistema para arrancar la ISO ARRANCABLE
* Instale el SO
* Desmonte el soporte virtual
* Reinicie el servidor

## Opción 3: Montar una ISO desde el sistema local
{: #bm-mount-iso-opt-3}

<a name="option3"></a>

Puede montar una ISO desde el sistema local utilizando el visor (consola) de Java iKVM. De esta forma, podrá montar una ISO mientras está conectado a la consola. La velocidad a la que avanza la instalación puede variar en función de la velocidad de carga y la latencia de la conexión a Internet, el rendimiento de Java y el sistema.

Si no tiene permiso para cambiar el BIOS de un servidor, abra una incidencia de soporte para solicitar los siguientes cambios:
* Privilegios de administrador de usuario Root en IPMI (para poder cambiar la modalidad de Virtual Media Attach)
* Cambiar la secuencia de arranque a 'IPMI Virtual Disk' como primera opción de arranque. (Puesto que la ISO aún no está montada, por ahora el equipo de soporte solo debe cambiar la prioridad del dispositivo de arranque).


1. Inicie sesión en la consola de gestión de IPMI apuntando su navegador web a la IP especificada en cloud.ibm.com.
* Pulse Dispositivos > su servidor (detalles del dispositivo) > Gestión remota. Especifique el nombre de usuario y la contraseña.
* Pulse Configuration > Remote session y cambie la modalidad de Attach a **attach**. En algunas consolas anteriores de IPMI, esta opción no está disponible, así que puede saltarse este paso.
* Pulse System > System information para volver a la página de información del sistema. Verá un icono de ventana de consola.
* Pulse el icono de la consola para abrir la consola. Acepte todas las advertencias de seguridad.
* Cuando la consola esté conectada, verá la solicitud de inicio de sesión.
* Pulse Virtual Media > Virtual Storage
* Vaya al separador **CDROM&ISO** y seleccione el archivo ISO en **Logical Drive Type**
* Pulse **Open Image** y seleccione la ISO en el sistema local
* Pulse **Plug in** para insertar la ISO en la unidad de CD-ROM virtual.
* Pulse **Ok**.
* Rearranque el servidor y utilice la opción de **arranque desde la unidad de CD-ROM virtual**. Puede que necesite utilizar el teclado virtual en el visor de iKVM para seleccionar un dispositivo de arranque.

## Resolución de problemas
{: #bm-mount-iso-troubleshooting}

* No todos los usuarios tienen acceso predeterminado para montar medios virtuales. Si se produce un error de permiso, póngase en contacto con el equipo de soporte para actualizar los permisos de usuario root de IPMI.
* Si una ISO ya está montada, aparecerá un mensaje de error con el texto **There is a disk mounted**. Debe desmontar el disco existente y sustituirlo por la nueva ISO. No se pueden montar dos ISO al mismo tiempo.
* Quizá sea necesario ponerse en contacto con el equipo de soporte para cambiar el orden de arranque en el BIOS.
* Al montar un ISO, utilice [SSL VPN](http://vpn.softlayer.com) en lugar de PPTP VPN.  Una vez conectado a la red de VPN, también puede acceder al IPMI del sistema mediante la dirección de IPMI (https://private-ip-IPMI-management).
* Cuando indique una vía de acceso a una ISO, utilice la sintaxis de nombre UNC (Universal Naming Convention) para la vía de acceso, por ejemplo:
  `\\<NAS username>\<isoname>.iso`
