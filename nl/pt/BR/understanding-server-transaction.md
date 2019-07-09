---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

keywords: server transation, {{site.data.keyword.cloud_notm}}, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Entendendo uma transação do servidor
{: #bm-server-transaction}

Quando um servidor no {{site.data.keyword.cloud}} é provisionado, um sistema operacional é carregado ou um software é instalado, ele é colocado em uma *transação*.  Uma transação é uma série automatizada de etapas que são executadas pelos sistemas de gerenciamento do
{{site.data.keyword.cloud_notm}} para configurar os servidores do cliente.

Se um de seus servidores estiver em uma transação, um link aparecerá nas notas do servidor em listagens de hardware.  É possível clicar nesse link para ver quais transações estão pendentes para esse servidor específico.  Em seguida, uma tabela que lista os dados para a transação atual que está em andamento é exibida.

* **ID** é o ID interno da transação.  Se você enviar um chamado sobre uma transação, inclua esse número.
* **Grupo** é uma descrição simples do tipo de transação.  Por exemplo, *Recarregamento do S.O. MS* significa que um sistema operacional Microsoft está sendo recarregado na máquina.
* **Status atual** é o nome da etapa de transação atual.  Por exemplo, *INSTALL_OS* é uma etapa de transação para *Recarregamento do S.O. MS*, o que significa que o Windows está sendo instalado atualmente na máquina.
* **Tempo decorrido e tempo médio** trabalham juntos.  Tempo decorrido mostra há quanto tempo a etapa de transação atual está em execução.  Tempo médio mostra a quantia de tempo que esta etapa demora em média.  Se o tempo decorrido for significativamente maior do que o tempo médio, você poderá querer abrir um chamado de suporte para o
status.
