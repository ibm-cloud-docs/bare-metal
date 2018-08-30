---



copyright:
  years: 2014, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Incluindo Conjuntos Sobressalentes 
{: #adding-spare-pools}

Conjunto sobressalente é uma forma de failover, em que certos dispositivos são designados como hot spares e podem assumir o fluxo de trabalho de um dispositivo primário no caso de falha. Para que um dispositivo seja designado como um hot spare, ele deve ser incluído no conjunto sobressalente e ser associado a um dispositivo primário. 
Conclua as etapas a seguir para incluir um dispositivo no conjunto sobressalente:
{:shortdesc}

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Dispositivos > Conjunto sobressalente** na Barra de navegação para acessar a tela *Conjunto sobressalente*.
3. Clique no link **Incluir no Conjunto sobressalente**.
   
   Uma lista de dispositivos elegíveis para serem incluídos no conjunto sobressalente será preenchida.
   {:tip}
   
4. Selecione os dispositivos a serem incluídos no conjunto sobressalente.
5. Clique em  ** Incluir Dispositivos Selecionados **.
6. Clique em **Confirmar** para incluir os dispositivos no conjunto sobressalente. 

## Próximas Etapas
Depois de iniciar a transferência de um dispositivo para o conjunto sobressalente, o dispositivo é transicionado para o conjunto sobressalente dentro de uma hora. Depois que o dispositivo está ativo no conjunto sobressalente, ele é exibido na tela Conjunto sobressalente e pode ser designado como um hot spare para um dispositivo primário.
