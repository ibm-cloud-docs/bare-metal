---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Instalación del servidor Ubuntu en un servidor nativo

Si desea utilizar un sistema operativo no proporcionado por {{site.data.keyword.IBM&reg; Cloud}}, puede instalarlo en los servidores nativos montando ISO (imágenes de disco) personalizadas. Para montar una carga de ISO, cárguela en el almacenamiento de archivos (NAS) asociado con el servidor. Para cargar una ISO en el NAS, utilice los procedimientos siguientes para montar una ISO con IPMI.
1. Pida el servidor nativo **Sin sistema operativo** 
* También puede seleccionar un SO gratuito (por ejemplo, CentOS) como sistema operativo que puede utilizarse para conectarse al NAS.
* Pida el almacenamiento NAS para almacenar la ISO arrancable. Si ya tiene un servidor CIFS de Windows, puede utilizarlo para compartir la imagen ISO. Con este servidor CIFS de Windows, obtendrá el NAS existente con 20 GB de capacidad. Después de suministrar el NAS, puede ver la descripción del mismo desde el portal de clientes.
* Descargue la imagen ISO desde https://www.ubuntu.com/download/server.
* Cargue la imagen ISO en el NAS o en el servidor CIFS de Windows. Si tiene el almacenamiento NAS, puede cargar el archivo de imagen ISO mediante FTP.

  Ejemplo de procedimiento por FTP:
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* Establezca una conexión VPN a {{site.data.keyword.Bluemix_notm}} con IPMI. Puede iniciar el menú de VPN desde el menú de soporte o desde el URL siguiente: [Acceso VPN](http://www.softlayer.com/VPN-Access)
* Monte la imagen ISO desde el menú Virtual Media de IPMI utilizando la conexión a IPMI mediante la IP de gestión.
  1. Vea las credenciales de IPMI
  * Inicie sesión en IPMIView
  * Abra el separador Virtual Media
  * Necesitará el usuario root con privilegios de administrador en IPMI. Si los privilegios se muestran como *Operator*, abra una incidencia de soporte para cambiar los privilegios a Administrator.
  * Rellene la información de conexión de la imagen ISO
    Share host = la dirección IP del NAS<br/Ejemplo: 10.3.x.x
    Path to image = el nombre del archivo ISO, con el formato siguiente: \NASusername\imagefilesname.iso (ej.: \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    User = el nombre de usuario del NAS
    Password = la contraseña del NAS
  * Pulse el botón **Mount**
  * Confirme el dispositivo
* Pulse y lance el visor de KVM, y abra la página Virtual Storage desde el menú Virtual Media. Si monta correctamente la imagen ISO como dispositivo CD-ROM, verá la descripción del dispositivo en **Connection Status History**.
* Mediante una incidencia de SoftLayer, solicite que el servidor arranque el CD-ROM virtual como primer dispositivo. Realice esta solicitud para cada servidor. Puede cambiar el valor de arranque una vez instalado el SO. 
  **Nota**: quizá no sea necesario ponerse en contacto con el equipo de soporte para cambiar el orden de arranque en el BIOS. Depende del servidor. Intente rearrancar una vez para confirmar el orden de arranque.
* Rearranque el servidor desde la vista de KVM.
* Instale el SO desde la imagen ISO montada.
* Instale el SO Ubuntu en el servidor nativo desde la ISO.
* Configure los valores de red (dirección IP/subred/pasarela/DNS etc.). Si no los configura correctamente durante el paso de instalación, sólo podrá conectarse a este servidor mediante la consola de KVM después del rearranque.

* Desmonte el soporte virtual. Debe desmontar el soporte virtual del servidor mediante el separador Virtual Media de IPMI.
* Rearranque el servidor.
* Después de rearrancar, puede acceder al servidor a través de SSH.
