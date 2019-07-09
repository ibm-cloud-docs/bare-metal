---

copyright:
  years: 1994, 2019
lastupdated: "2019-06-17"

keywords: server IP addresses, bare metal, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Asignación y enlace de direcciones IP
{: #bm-assigning-and-binding-ip-addresses
Utilice la siguiente información para asignar una dirección IP de servidor al servidor y enlazar una dirección IP secundaria al servidor, si es necesario.
{: shortdesc}

## Asignación de direcciones IP de servidor
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} configura los servidores con estas direcciones:
Una dirección IPv4 en la red privada,
Una dirección IPv4 para el acceso de gestión de bajo nivel en la
red privada,
Una dirección IPv4 pública si se solicita.

También se puede solicitar una dirección IPv6 en la red pública. Todas estas
direcciones IP se denominan colectivamente **Direcciones IP principales**.

Se pueden enlazar más direcciones IP a los servidores después de adquirir **Subredes secundarias** a través de la [consola de {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com){: external}. Las direcciones IP que ha adquirido mediante el Portal de clientes y que usted gestiona se denominan **Direcciones IP secundarias**.

Para obtener más información sobre la adquisición de direcciones IP, consulte [Subredes e IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}.


## Enlace de direcciones IP secundarias
{: #bm-bind-secondary-ip-address}

Después de adquirir una subred secundaria, deberá configurar
el sistema operativo para que utilice una o varias direcciones IP. Cada sistema operativo configura las direcciones IP de forma distinta, pero se suele hacer referencia a la configuración de los "alias de interfaz".
