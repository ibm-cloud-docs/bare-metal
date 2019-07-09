---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: ssl certificate, sercure sockets layer

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Certificados SSL
{: #bm-ssl-certificates}

SSL (capa de sockets seguros) es una tecnología que cifra el tráfico entre la aplicación cliente y la aplicación de servidor implicadas en la conversación. El cifrado se logra mediante el uso de un sistema de clave pública/clave privada que utiliza un certificado SSL.
{:shortdesc}

El certificado SSL contiene la clave pública del servidor, las fechas en las que es válido el certificado, un nombre de host para el que es válido el certificado y una firma de la autoridad de certificación que lo ha emitido. Con esta información y algunos detalles de protocolo que se intercambian durante el inicio de una sesión, el cliente puede estar razonablemente seguro de que el servidor es el servidor con el que pretende hablar.

Para obtener más información sobre certificados SSL, consulte [Iniciación a certificados SSL](/docs/infrastructure/ssl-certificates?topic=ssl-certificates-getting-started-tutorial).
