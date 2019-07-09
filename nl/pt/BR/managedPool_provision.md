---

copyright:
  years:  2019
lastupdated: "2019-02-01"

keywrods: provision managed pool, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Fornecendo Conjuntos Gerenciados pelo Cliente
{: #bm-provision-managed-pools}

Para fornecer um conjunto de servidores gerenciado pelo cliente, entre em contato com a IBM diretamente: [Obtendo ajuda e suporte](/docs/bare-metal?topic=bare-metal-gettinghelp).

Forneça as seguintes informações:
* O data center no qual deseja que os conjuntos gerenciados sejam localizados. (Todos os servidores em um conjunto gerenciado
devem estar localizados no mesmo data center.)
* O número de servidores que deseja no conjunto gerenciado
* As especificações necessárias para os servidores agrupados

Após a criação do conjunto, a IBM fornecerá os valores de parâmetro a seguir. Esses valores são necessários ao enviar o
comando API para gerenciar o conjunto.
* poolKeyName
* backendRouter

## Solicitando servidores a partir de seu conjunto gerenciado
{: #bm-order-server-managed-pool}
Use o processo de fornecimento padrão para solicitar os servidores no conjunto. O pedido é atendido do seu
conjunto e ele é reabastecido com o número de servidores solicitado.

## Próximas etapas

Após o fornecimento do conjunto gerenciado pelo cliente e a solicitação dos servidores do conjunto gerenciado, é
possível gerenciar o número de servidores no conjunto. Consulte [Especificando o
número de servidores no conjunto gerenciado pelo cliente](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)
