---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

keywords: bare metal reactivate spare pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Reativando um dispositivo do conjunto sobressalente
{: #bm-reactivating-spare-pools}

Quando um dispositivo é incluído no conjunto sobressalente, seu status na Lista de dispositivos muda de Ativo, indicando que o dispositivo é elegível para interações padrão, para o Conjunto sobressalente. Os dispositivos que fazem parte do conjunto sobressalente são dedicados a essa
funcionalidade e podem não ser usados para ações tradicionais e diárias como outros
dispositivos. Para remover um dispositivo do conjunto sobressalente para que ele possa
retornar para sua funcionalidade tradicional, ele deve ser reativado.{:shortdesc}

## Reativando um dispositivo do conjunto sobressalente

1. Acesse o [{{site.data.keyword.cloud}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Dispositivos > Conjunto sobressalente** na Barra de navegação para acessar a tela *Conjunto sobressalente*.
3. Selecione **Ações > Reativar dispositivo** para o dispositivo desejado.
4. Clique em **Sim** para reativar o servidor. Clique em **Não** para
cancelar a ação.

## Próximas Etapas
Depois de iniciar o processo de reativação, o dispositivo é colocado off-line, o firmware é atualizado e o dispositivo fica disponível para uso regular. O processo de reativação leva aproximadamente uma hora. Os dispositivos removidos do conjunto sobressalente não ficam mais elegíveis para uso como um método de failover. O dispositivo pode retornar ao conjunto sobressalente a qualquer momento, ao ser incluído no conjunto sobressalente novamente. Para obter mais informações, veja [Incluindo um dispositivo no conjunto sobressalente](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools).
