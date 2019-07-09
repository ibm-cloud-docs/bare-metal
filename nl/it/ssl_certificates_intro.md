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

# Certificati SSL
{: #bm-ssl-certificates}

SSL (Secure Sockets Layer) è una tecnologia che crittografa il traffico tra l'applicazione client e l'applicazione server coinvolta nella conversazione. Questa crittografia viene effettuata tramite un sistema a chiave pubblica/chiave privata che utilizza un certificato SSL.
{:shortdesc}

Il certificato SSL contiene la chiave pubblica del server, le date per le quali il certificato è valido, un nome host per il quale il certificato è valido e una firma dell'Autorità di certificazione che lo ha rilasciato. Con queste informazioni e alcune informazioni sul protocollo che vengono scambiate durante l'inizio di una sessione, il client può essere ragionevolmente certo che il server è quello con cui intende comunicare.

Per ulteriori informazioni sui certificati SSL, vedi [Introduzione ai certificati SSL](/docs/infrastructure/ssl-certificates?topic=ssl-certificates-getting-started-tutorial).
