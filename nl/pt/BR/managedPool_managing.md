---

copyright:
  years:  2019
lastupdated: "2018-05-15"

keywords: number servers managed pool, managed pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Especificando o número de servidores no conjunto gerenciado pelo cliente
{: #set-amount-servers-pool}

Configure o número de servidores no conjunto gerenciado usando a chamada API a seguir:

|Chamada de API|Parƒmetros|Descrição|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank"> Configurar Quantidade do Conjunto Gerenciado </a>|poolKeyName|Nome da chave que identifica o conjunto. A IBM fornece esse valor para você.|
|  | backendRouter | Identifica o roteador de backend para o conjunto. A IBM fornece esse valor para você.|
|  | quantidade | O número total de servidores que você deseja no conjunto.<br><br>Se o
número atual de servidores em seu conjunto for menor que o valor fornecido aqui, os
servidores serão incluídos.<br>Se o número atual de servidores em seu conjunto for maior
que o valor fornecido aqui, os servidores serão removidos.|
