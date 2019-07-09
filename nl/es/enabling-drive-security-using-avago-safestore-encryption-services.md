---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Habilitación de la seguridad de unidad utilizando Avago SafeStore Encryption Services
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

La configuración de la seguridad de unidad ayuda a evitar el acceso a datos almacenados en discos eliminados sin una clave de seguridad. Los datos de la unidad no se pueden recuperar sin esta clave. {{site.data.keyword.BluSoftlayer_full}} proporciona unidades de cifrado automático (SED) en centros de datos selectos para las unidades que se pueden adquirir en un servidor nativo. Hay unidades SATA de 10 TB disponibles en nuestros centros de datos de EE.UU.

## Requisitos previos
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* Servidor nativo con unidades SED - SATA de 10 TB
* Tarjetas LSI/AVAGO MegaRAID SAS 9361 -8i o LSI/AVAGO RAID similares
* Software MegaRAID Storage Manager instalado

## Habilitación de la seguridad de unidad utilizando MegaRAID Storage Manager (MSM)
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

Puede establecer la clave seguridad y proteger los datos de un disco eliminado utilizando MegaRAID Storage Manager. También puede utilizar la interfaz de WebBIOS que requiere una clave de seguridad en el momento del inicio del servidor para entrar en la BIOS de la tarjeta MegaRAID para configurar el valor de seguridad de unidad. Para obtener más información sobre MegaRAID Controller Card SAS 9361-8i, consulte el sitio de Broadcom, [MegaRAID SAS 9361-8i ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation).

### Identificación de unidades SED preinstaladas
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager viene preinstalado en la mayoría de los sistemas operativos soportados. Si no está presente, puede instalarlo manualmente desde el sitio de Broadcom. Para obtener más información, consulte
[Descargas de MegaRAID SAS 9361-8i](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads).

Puede abrir MegaRAID Storage Manager utilizando las credenciales del sistema. En el ejemplo, se utiliza un entorno Windows y MSM viene preinstalado.

Al iniciar MSM, debe especificar el **Nombre de usuario** y la **Contraseña**, que son el usuario privilegiado (Administrador) y su contraseña.

Pulse el separador **Físico** y pulse en las unidades que están disponibles en el sistema. El panel **Propiedades** tiene la sección **Propiedades de seguridad de unidad** que incluye el campo **Capacidad de cifrado de disco completo**, que indica **Sí**. En el ejemplo utilizado, se usan dos discos no SED y cuatro discos SED.

### Habilitación de la seguridad de unidad en el controlador
{: #enabling-drive-security-at-the-controller}

1. Para habilitar la seguridad de unidad, pulse el botón derecho del ratón sobre **Controlador 0 :AVAGO MegaRAID SAS 9361-8i** en el separador **Físico** y seleccione
**Habilitar la seguridad de unidad**.
  * Ahora puede especificar el **Identificador de clave de seguridad** y la **Clave de seguridad**. Si tiene varias claves de seguridad, un identificador de clave de seguridad puede ayudarle a identificar qué clave de seguridad necesita utilizar. Debe registrar la clave de seguridad en una ubicación segura. La clave de seguridad es necesaria para reconfigurar unidades, por ejemplo, para extraer o reinsertar una unidad. Sin una clave de seguridad, no es posible recuperar ningún dato almacenado en un volumen creado fuera de los SED. No es posible recuperar una clave de seguridad olvidada. También se puede establecer una contraseña de tiempo de inicio, que mantiene en pausa el sistema para que se especifique la contraseña que se defina aquí. La contraseña de tiempo de inicio es opcional y, si la establece, deberá iniciar sesión en IPMI y escribir la contraseña de inicio siempre que se rearranque el sistema. Desplácese hacia abajo y marque el recuadro de selección que indica
**He grabado los valores de seguridad como referencia futura** y pulse **Sí** para habilitar la seguridad de unidad.
  * Cuando se habilite la seguridad de unidad, aparecerá una imagen de llave amarilla para
**Controlador 0 AVAGO MegaRAID SAS 9361-8i**.
2. Ahora, cree un volumen seguro utilizando las SED. Pulse con el botón derecho del ratón en **Controller0** en el separador **Lógico** y seleccione  
**Crear unidad virtual**.
3. Elija la opción **Avanzado**. Es necesario especificar el **Nivel de RAID** en la pantalla, así como especificar el **Método de seguridad de unidad** como **Cifrado de disco completo (FDE)**. Seleccione las unidades FDE que sean necesarias y pulse **Añadir** > **Crear grupo de unidades** > **Siguiente**.
4. Revise los valores de unidad virtual y realice los cambios necesarios. El valor sugerido para la **Política de lectura** es **Siempre lectura anticipada**. El valor sugerido para la **Política de escritura** es **Reescritura**. Pulse **Crear unidad virtual**. Acepte el impacto de la política de reescritura debido a BBU pulsando **Sí**. Pulse **Siguiente** y revise la pantalla de resumen. Pulse **Finalizar**.
5. Para confirmar que el disco virtual sea seguro, pulse el separador **Lógico** y la unidad virtual que se ha creado. Verá en las **Propiedades de seguridad de unidad** que el campo **Seguro** está marcado como **Sí**.

Si el servidor se proporcionaba con volúmenes RAID que ya están creados utilizando unidades SED, puede hacer que el volumen sea seguro siguiendo estos pasos.

En el separador **Lógico**, pulse el botón derecho del ratón sobre **Grupo de unidades** y seleccione
**Proteger utilizando FDE**. Si ha mezclado unidades FDE y no FDE, esta opción no será visible.

Para eliminar la seguridad de unidad, primero debe suprimir los discos virtuales seguros y pulsar el botón derecho del ratón sobre el Controlador 0 para **Inhabilitar la seguridad de unidad**. Esta función borra de forma segura los datos y elimina la seguridad de unidad.

También puede configurar la seguridad de unidad utilizando webBIOS e iniciando sesión a través de IPMI en el momento del inicio y entrando en la BIOS RAID. <!--For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.-->
