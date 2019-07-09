---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: bare metal, spare pools

subcollection: bare-metal

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

O conjunto sobressalente é uma forma de manter determinados dispositivos designados como sobressalentes e ter a capacidade de assumir o fluxo de trabalho de um dispositivo primário ou agir como um novo dispositivo na frota do cliente. Para que um dispositivo seja designado como sobressalente, ele deve ser incluído no conjunto sobressalente e associado a um dispositivo primário. Siga as etapas a seguir para incluir um dispositivo no conjunto sobressalente.
{:shortdesc}

1. Acesse o [console do {{site.data.keyword.cloud}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Dispositivos > Conjunto sobressalente** na Barra de navegação para acessar a tela *Conjunto sobressalente*.
3. Clique no link **Incluir no Conjunto sobressalente**.

   Uma lista de dispositivos elegíveis para serem incluídos no conjunto sobressalente será preenchida.
   {:tip}

4. Selecione os dispositivos a serem incluídos no conjunto sobressalente.
5. Clique em  ** Incluir Dispositivos Selecionados **.
6. Clique em **Confirmar** para incluir os dispositivos no conjunto sobressalente.

## Próximas Etapas
Depois de iniciar a transferência de um dispositivo para o conjunto sobressalente, o dispositivo é transicionado para o conjunto sobressalente dentro de uma hora. Depois que o dispositivo está ativo no conjunto sobressalente, ele é exibido na tela Conjunto sobressalente e pode ser designado como um hot spare para um dispositivo primário.
