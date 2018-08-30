---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---


# Fornecendo Conjuntos Gerenciados pelo Cliente

Para fornecer um conjunto de servidores gerenciado pelo cliente, entre em contato com a IBM diretamente: [Obtendo ajuda e suporte](../bare-metal/get-help-and-support.html).

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
Use o processo de fornecimento padrão para solicitar os servidores no conjunto. O pedido é atendido do seu
conjunto e ele é reabastecido com o número de servidores solicitado.

## Próximas etapas

Após o fornecimento do conjunto gerenciado pelo cliente e a solicitação dos servidores do conjunto gerenciado, é
possível gerenciar o número de servidores no conjunto. Consulte [Especificando o
número de servidores no conjunto gerenciado pelo cliente](../bare-metal/managedPool_managing.html)
