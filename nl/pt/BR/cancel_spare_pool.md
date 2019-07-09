---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: spare pools, cancel, bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Cancelando conjuntos sobressalentes
{: #cancel-spare-pools}

Os dispositivos que foram incluídos no conjunto sobressalente podem ser cancelados somente na tela Conjunto sobressalente dentro do console do {{site.data.keyword.cloud}}. O cancelamento de um dispositivo no conjunto sobressalente é idêntico àquele de um dispositivo na Lista de dispositivos. Siga as etapas a seguir para cancelar um dispositivo no conjunto sobressalente.
{:shortdesc}

## Cancelando conjuntos sobressalentes

1. Faça backup de todos os dados que você deseja manter do dispositivo que está sendo cancelado.

   O cancelamento de um dispositivo resulta na remoção de todos os dados do dispositivo cancelado. Todas as informações armazenadas no dispositivo não podem ser recuperadas após o cancelamento do dispositivo.
   {:tip}

2. Acesse o [console do {{site.data.keyword.cloud}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window} usando suas credenciais exclusivas.
3. Selecione **Dispositivos > Conjunto sobressalente** na Barra de navegação para acessar a tela *Conjunto sobressalente*.
4. Selecione **Ações > Cancelar dispositivo** para o dispositivo específico.
5. Selecione o motivo de cancelamento na lista suspensa **Motivo**.
6. Insira uma breve explicação do cancelamento na caixa de texto fornecida.
7. Clique em **Continuar** para continuar na próxima tela. Clique em **Cancelar** para parar o processo de cancelamento e retornar à tela Conjunto sobressalente.
8. Selecione **Confirmação da perda de dados** para reconhecer pode ocorrer a perda de dados como parte do processo de cancelamento.
9. Clique em **Cancelar dispositivo** para cancelar o dispositivo. Clique em **Fechar** para parar o processo de cancelamento e retornar à tela Conjunto sobressalente.

## Próximas Etapas
Depois de solicitar cancelamento de um dispositivo no conjunto sobressalente, o dispositivo é planejado para cancelamento. O dispositivo é então recuperado imediatamente e removido da conta.
