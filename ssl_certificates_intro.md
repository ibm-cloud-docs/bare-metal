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

# SSL certificates
{: #bm-ssl-certificates}

Secure Sockets Layer (SSL) is a technology that encrypts traffic between the client application and the server application that is involved in the conversation. This encryption is accomplished through a public key/private key system that uses an SSL certificate.
{:shortdesc}

The SSL certificate contains the server’s public key, dates for which the certificate is valid, a host name for which the certificate is valid and a signature from the Certification Authority that issued it. With this information and some protocol information that is exchanged during the beginning of a session, the client can be reasonably certain that the server is the one to which it is intending to talk.

For more information about SSL certificates, see [Getting started with SSL certificates](/docs/ssl-certificates?topic=ssl-certificates-getting-started-tutorial).
