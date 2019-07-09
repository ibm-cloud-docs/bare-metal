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

# Certificats SSL
{: #bm-ssl-certificates}

SSL (Secure Sockets Layer) est une technologie qui chiffre le trafic entre l'application client et l'application serveur impliquée dans la conversation. Ce chiffrement est réalisé via un système de clé publique/clé privée utilisant un certificat SSL.
{:shortdesc}

Le certificat SSL contient la clé publique du serveur, les dates de validité du certificat, un nom d'hôte pour lequel le certificat est valide et une signature provenant de l'autorité de certification qui l'a émis. Avec ces informations et certaines informations de protocole échangées au début d'une session, le client peut raisonnablement être certain que le serveur est bien celui avec lequel il entend discuter.

Pour plus d'informations sur les certificats SSL, voir [Initiation aux certificats SSL](/docs/infrastructure/ssl-certificates?topic=ssl-certificates-getting-started-tutorial).
