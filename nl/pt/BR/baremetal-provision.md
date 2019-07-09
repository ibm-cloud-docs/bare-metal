---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Construindo um servidor bare metal customizado
{: #ordering-baremetal-server}

Use as etapas a seguir para construir {{site.data.keyword.baremetal_long}} customizados.

## Fornecimento por meio do catálogo do {{site.data.keyword.cloud_notm}}
{: #provision-through-the-catalog}

Use as etapas a seguir para provisionar seu {{site.data.keyword.baremetal_short}} por meio do {{site.data.keyword.cloud_notm}}.

1. Abra o [catálogo do {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog/){: external}.   
2. Selecione {{site.data.keyword.baremetal_short}} em **Cálculo**.
3. Clique em Continuar. Se você não vir um botão Continuar, poderá ser necessário efetuar login.
4. Insira a **Quantidade** de servidores **idênticos** para provisão. O padrão é 1. Se você desejar provisionar vários servidores com especificações _diferentes_, será necessário provisionar os servidores separadamente.
5. **Nome do host** é um nome permanente ou temporário para seus servidores, por exemplo, baremetal01. Clique em **Informações** para obter as especificações de formatação.
6. **Domínio** é a sequência de identificação que define o controle administrativo dentro da Internet, por exemplo, Customer-123456.cloud. Clique em **Informações** para obter as especificações de formatação.
7. **Faturamento** é **Por hora** ou **Mensal**.
8. Selecione o **Local**, a região e o datacenter, em que seu servidor deve estar localizado.
9. Clique em **Todos os servidores** para ver uma lista de processadores (Single, Dual e Quad) e servidores certificados (SAP e VMware). Selecione o servidor que melhor atenda à sua carga de trabalho.
10. Selecione sua **RAM**. Para alguns servidores, o padrão da RAM se baseia no Modelo de CPU e não pode ser mudado. 

Para servidores certificados SAP, RAM e Sistema operacional são padronizados com base na seleção do servidor. Sua opção de armazenamento local também é padronizada com base na seleção do servidor.
{ :note}

11. Insira uma chave pública opcional para sua **chave SSH**,que pode ser usada para efetuar login no servidor após ele ser provisionado.
12. Selecione uma **Imagem** (sistema operacional) para seu servidor. Suas opções são baseadas no servidor selecionado.
13. Expanda **Complementos** para selecionar opções relacionadas à configuração do servidor.
14. Os **Discos de armazenamento** são pré-configurados com na seleção de servidor. Expanda **Complementos** para incluir volumes de armazenamento de Arquivo ou de Bloco após o {{site.data.keyword.baremetal_short}} ter sido provisionado. 
15. Em **Interface de rede**, selecione as opções Velocidades da porta de uplink e VLAN privada. Expanda **Complementos** para selecionar as opções apropriadas ou usar os valores padrão.
16. Revise seu pedido no Resumo do pedido.
17. Insira quaisquer códigos promocionais que você tenha em **Aplicar código promocional**.
18. Clique nos contratos de serviço de terceiros para quaisquer contratos listados.
19. Clique em **Criar** para provisionar seu servidor. Você é redirecionado para uma tela com seu número da ordem de fornecimento, que pode ser impresso porque também é seu recibo.

Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído.

O e-mail de _fornecimento completo_ inclui um link para a página *Detalhes do dispositivo* para que você possa efetuar login no {{site.data.keyword.cloud_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

Você também tem a opção de salvar o pedido como uma cotação ou incluí-lo em uma estimativa. Quando você salva uma cotação, um link é enviado para o endereço de e-mail associado à sua conta. Abra o link para ver as informações de cotação salvas. Outra opção é acessar Gerenciar > Faturamento e uso e selecionar Vendas > Cotações de dispositivo. Se você tiver acesso, será possível comprar a oferta cotada clicando na cotação e confirmando o pedido. A inclusão na estimativa coloca o custo proposto de configurações na calculadora de precificação. Clique em **Informações** para obter mais detalhes sobre a calculadora de precificação.

## Fornecimento por meio do portal do cliente
Use as etapas a seguir para provisionar seu
{{site.data.keyword.baremetal_short}} por meio do
{{site.data.keyword.slportal}}.

1. Efetue login no [{{site.data.keyword.slportal}}](control.softlayer.com){: external} usando suas credenciais exclusivas.
2. Acesse **Conta** > **Fazer um pedido**.
3. Escolha **Por hora** ou **Mensal**.
3. Selecione seu data center no qual deseja seu {{site.data.keyword.baremetal_short}} localizado na lista e, em seguida, selecione seu servidor certificado (SAP ou VMware) ou processador (Single, Dual e Quad) clicando em **PREÇO INICIAL**.
4. Insira a **Quantidade** de servidores _idênticos_ para provisão. O padrão é 1. Se você desejar provisionar vários servidores com especificações _diferentes_, será necessário provisionar os servidores separadamente.
5. Selecione sua **RAM**. Para alguns servidores, o padrão da RAM se baseia no Modelo de CPU e não pode ser mudado. 

Para servidores certificados SAP, RAM e Sistema operacional são padronizados com base na seleção do servidor. Sua opção de armazenamento local também é padronizada com base na seleção do servidor.
{ :note}

6. Selecione seu sistema operacional.
7. Selecione suas unidades de disco rígido e complementos adicionais do sistema.
8. Clique em **Incluir no pedido** no qual você é redirecionado para confirmar seu pedido.
9. Confirme ou edite as informações de domínio para o servidor. **Nome do host** é um nome permanente ou temporário para seus servidores, por exemplo, baremetal01. 
10. Selecione **Termos do serviço de nuvem** e o **Contrato de serviços de terceiros**.
11. Insira quaisquer códigos promocionais em **Código promocional** e clique em **Aplicar**.
12. Confirme ou insira suas informações de pagamento e clique em **Enviar pedido**. Você é redirecionado para uma tela com seu número da ordem de fornecimento, que pode ser impresso porque também é seu recibo. 

Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento inclui um link para sua página *Detalhes do dispositivo*, depois de efetuar login no {{site.data.keyword.Bluemix_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

## Próximas Etapas
Após os {{site.data.keyword.baremetal_short}} serem provisionados, é possível começar a gerenciá-los. Para obter mais informações, veja [Gerenciando o {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
