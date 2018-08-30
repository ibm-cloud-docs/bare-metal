---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-01"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Reativando um dispositivo do conjunto sobressalente 
{: #reactivating-spare-pools}

Quando um dispositivo é incluído no conjunto sobressalente, seu status na Lista de dispositivos muda de Ativo, indicando que o dispositivo é elegível para interações padrão, para o Conjunto sobressalente. Os dispositivos que fazem parte do conjunto sobressalente são dedicados a essa função e não podem ser usados para ações diárias tradicionais, como outros dispositivos. Para remover um dispositivo do conjunto sobressalente para que ele possa retornar à sua função tradicional, ele deve ser reativado. Conclua as etapas a seguir para reativar um dispositivo.
{:shortdesc}

## Reativando um dispositivo do conjunto sobressalente 

1. Acesse o [{{site.data.keyword.slportal_full}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){: new_window} usando suas credenciais exclusivas.
2. Selecione **Dispositivos > Conjunto sobressalente** na Barra de navegação para acessar a tela *Conjunto sobressalente*.
3. Selecione **Ações > Reativar dispositivo** para o dispositivo desejado.
4. Clique em **Sim** para reativar o servidor. Clique em **Não** para
cancelar a ação.

## Próximas Etapas
Depois de iniciar o processo de reativação, o dispositivo é colocado off-line, o firmware é atualizado e o dispositivo fica disponível para uso regular. O processo de reativação leva aproximadamente uma hora. Os dispositivos removidos do conjunto sobressalente não ficam mais elegíveis para uso como um método de failover. O dispositivo pode retornar ao conjunto sobressalente a qualquer momento, ao ser incluído no conjunto sobressalente novamente. Para obter mais informações, veja [Incluindo um dispositivo no conjunto sobressalente](../vsi/adding_spare_pool.html).
