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

O Secure Sockets Layer (SSL) é uma tecnologia que criptografa o tráfego entre o aplicativo cliente e o aplicativo do servidor
que está envolvido na conversa. Essa criptografia é realizada por meio de um sistema de chave pública/chave privada que usa um
certificado SSL.
{:shortdesc}

O certificado SSL contém a chave pública do servidor, as datas para as quais o certificado é válido, um nome do host para o qual
o certificado é válido e uma assinatura da autoridade de certificação que o emitiu. Com essas informações e algumas informações de
protocolo que são trocadas durante o início de uma sessão, o cliente pode estar bastante seguro de que o servidor é aquele
com o qual pretende falar.

Para obter mais informações sobre certificados SSL, veja [Introdução a certificados SSL](/docs/infrastructure/ssl-certificates?topic=ssl-certificates-getting-started-tutorial).
