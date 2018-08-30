---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Asignación de direcciones IP de servidor

{{site.data.keyword.cloud}} configura los servidores con una dirección IPv4 en la red
privada, una dirección IPv4 para el acceso de gestión de bajo nivel en la
red privada y, si se solicita, una dirección IPv4 pública.
Una dirección IPv6 en la red pública, está disponible si se solicita. Todas estas
direcciones IP se denominan colectivamente como **Direcciones IP principales**.

Se pueden enlazar más direcciones IP a los servidores después de adquirir **Subredes secundarias** a través del [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com). Las direcciones IP que ha adquirido mediante el Portal de clientes y que usted gestiona se denominan **Direcciones IP secundarias**.

Para obtener más información sobre la adquisición de direcciones IP, consulte [Subredes e IP](https://console.bluemix.net/docs/infrastructure/subnets/).


# Enlace de direcciones IP secundarias

Después de adquirir una subred secundaria, deberá configurar
el sistema operativo para que utilice una o varias direcciones IP. Cada sistema operativo configura las direcciones IP de forma distinta, pero se suele hacer referencia a la configuración de los "alias de interfaz". 
