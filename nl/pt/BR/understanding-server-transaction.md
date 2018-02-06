---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Entendendo uma transação do servidor

Quando um servidor no {{site.data.keyword.Bluemix_short}} é provisionado, um sistema operacional é carregado ou um software é instalado, ele é colocado em uma *transação*. Uma transação é uma série automatizada de etapas realizadas pelos sistemas de gerenciamento do {{site.data.keyword.Bluemix_notm}} para configurar servidores de cliente.

Se um de seus servidores está atualmente em uma transação, um link aparece em notas do servidor nas listagens de hardware. É possível clicar nesse link para ver quais transações estão pendentes para esse servidor específico. É apresentada uma tabela que lista os dados para a transação atual que está em andamento.

* **ID** é o ID interno da transação. Se você enviar um chamado sobre uma transação, inclua esse número.
* **Grupo** é uma descrição simples do tipo de transação. Por exemplo, *Recarregamento do S.O. MS* significa que um sistema operacional Microsoft está sendo recarregado na máquina.
* **Status atual** é o nome da etapa de transação atual. Por exemplo, *INSTALL_OS* é uma etapa de transação para *Recarregamento do S.O. MS*, o que significa que o Windows está sendo instalado atualmente na máquina.
* **Tempo decorrido e tempo médio** trabalham juntos. Tempo decorrido mostra há quanto tempo a etapa de transação atual está em execução. Tempo médio mostra a quantia de tempo que esta etapa demora em média. Se o tempo decorrido é significativamente maior do que o tempo médio, você talvez deseje abrir um chamado de suporte para o status.
