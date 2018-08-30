---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Construindo um servidor bare metal customizado
{: #ordering-baremetal-server}

Use as etapas a seguir para construir {{site.data.keyword.baremetal_short}} customizados.

1. Abra o  [ {{site.data.keyword.cloud_notm}}  catálogo ](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Selecione Bare Metal Server.
3. Clique em Criar.
4. Abaixo da lista de servidores, procure a instrução: **Interessado em outras opções de configuração? Clique aqui **. 
Selecione essa opção. O formulário do servidor customizado é exibido.
1. Selecione um local do data center para o servidor.
* Selecione um servidor entre as três categorias de servidores clicando no link **Preço inicial por**.
  * Servidores certificados pela SAP (para obter mais informações sobre o fornecimento de um servidor certificado pela SAP, consulte
[Infraestrutura certificada pela SAP do {{site.data.keyword.cloud_notm}}](/docs/bare-metal/bare-metal-sap-applications.html))
  * Servidores Multicore de Processador Único
  * Servidores Duplos de Processador Multic-Núcleo

* Selecione a partir de suas opções de configuração. **Data center**, **RAM** e
**Sistema operacional** são campos obrigatórios. Todos os outros campos são opcionais. Para obter mais
informações sobre os campos opcionais, consulte **[Opções adicionais de configuração do servidor](#addl-server-options)**.

    **Nota**: uma mensagem de erro será exibida se existir um conflito entre o servidor e o sistema operacional. Por exemplo, selecionar Linux em um Microsoft SQL server.
* Clique em  ** Incluir no Pedido **. A página Checkout é exibida.

  Na página de check-out, é possível retornar para a página de configuração clicando em uma das opções de Reconfigurar.
* Na seção Configuração do sistema avançado, especifique as opções de configuração adicionais. Para obter mais informações,
consulte **[Configuração do sistema avançado](#adv-system-config)**.

*   Clique nas caixas de seleção **termos do Cloud Service** e **Contrato de prestação de serviços de terceiro**.
*   Confirme ou insira suas informações de pagamento e clique em **Enviar pedido**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

  Também é possível salvar esse pedido sem comprar clicando em **Salvar como cotação**.

 Uma série de e-mails é enviada para o administrador: confirmação do pedido de fornecimento, aprovação e processamento do pedido de fornecimento e a conclusão do fornecimento. O e-mail completo de fornecimento inclui um link para sua página *Detalhes* depois de
efetuar login no {{site.data.keyword.cloud_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

 ## Opções adicionais de configuração do servidor
 {: #addl-server-options}

 Você terá opções adicionais disponíveis para quando estiver fornecendo o Bare Metal Server, por exemplo, a largura da banda
pública, as velocidades da porta de uplink, os endereços IP secundários públicos e mais. A Tabela 1 descreve suas opções adicionais.


 | **Campo** | **Descrição** |
 |-------------------|---------------|
 |Segurança do servidor|Tal como o Trusted Execution Technology (Intel TXT)|
 |Extensões do Software Guard|Segurança aumentada para o código e os dados confidenciais (Intel SGX). <br><br>Consulte
[Fornecendo um Bare Metal Server com o Intel SGX](../bare-metal/bare-metal-provision-SGX.html).|
 |RAM|Escolha um nível de RAM que atenda às necessidades do servidor.|
 |Sistema operacional |Selecione entre CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu ou Outro. |
 |Discos rígidos |Use a ferramenta na interface com o usuário para configurar os discos rígidos preenchendo os campos previamente com
base no S.O. selecionado. <br><br> Também é possível selecionar a utilização de uma unidade SSD Intel Optane. Consulte
[Fornecendo um Intel Optane SSD DC P4800X](../bare-metal/bm-provision_ssd.html).
 |Largura da Banda Pública |Determina a quantia de dados que pode ser transferida por meio da interface pública durante um mês. Para
ambientes de teste, que requerem que os dados de instalação sejam transferidos por meio dessa interface, os valores
precisam ser adaptados além da quantia de dados inicialmente transferida. Considere o
[{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) para enviar um
carregamento de dados inicial para um dos data centers do {{site.data.keyword.cloud_notm}}. Qualquer um dos {{site.data.keyword.baremetal_short}} pode ser submetido a upgrade para incluir a largura da banda não medida (ilimitada). Todos os dispositivos não medidos estão em portas privadas, dedicadas.|
 |Velocidades da Porta de Uplink |Determina a velocidade de interfaces internas e externas. |
 |Endereços IP secundários públicos |Designa mais endereços IP para o servidor. Dependendo de seu cenário, você pode requerer mais endereços IP designados para seu servidor. 
Mais endereços IPv4 estão disponíveis em quantidades de 1, 2, 4, 8, 16 ou 32. |
 |Endereços IPv6 primários |Designado às interfaces internas e externas do servidor. |
 |Endereços IPv6 estáticos públicos |Designa mais endereços IPv6 de um bloco /64. |
 |Complementos do Sistema Operacional|Selecione as opções, como o VMware, as soluções de backup, o painel de controle, o banco de
dados, os firewalls de hardware e de software, a proteção de antivírus e spyware, e a proteção e a detecção de intrusão. <br><br>É
altamente recomendável alinhar o departamento de segurança corporativa com o suporte do {{site.data.keyword.cloud_notm}} para discutir os detalhes dessas opções.
 |Evault |Uma ferramenta de backup baseado em agente que pode ser instalada em seu servidor para replicar backups entre servidores. |
 |Complementos de serviço|Selecione quaisquer complementos de serviço, como o monitoramento, a resposta automatizada e o seguro.|
 {: caption="Tabela 1. Opções adicionais do servidor" caption-side="top"}

## Configuração do sistema avançado
{: #adv-system-config}

Os campos em **Configuração do sistema avançado** concluem o processo de fornecimento.

| **Campo** | **Descrição** |
|---|---|
| Nome do host | Um nome permanente ou provisório para seu servidor, por exemplo, _server1_. **Nota**:
se você estiver fornecendo um servidor certificado pela SAP, o nome do host SAP deverá consistir em um máximo de 13
caracteres alfanuméricos. Para obter mais informações sobre nomes de host SAP, consulte
[Notas sobre o SAP 611361](https://launchpad.support.sap.com/#/notes/2611361) e [129997](https://launchpad.support.sap.com/#/notes/129997). Requer um ID do usuário do SAP S. |
| Domínio |Nome do subdomínio que não deve colidir com um nome de domínio da Internet, por exemplo, _test.acme.com_. |
| Seleção de VLAN |Se houver uma VLAN sob a conta porque você já pediu pelo menos no servidor, será possível incluir o novo servidor
nessa VLAN. |
| Script de fornecimento |É possível fornecer um script que permite automatizar determinadas etapas após o fornecimento. |
| Chaves SSH |É possível fornecer a chave pública da chave SSH, o que permite efetuar login no servidor após ele ter
sido fornecido. |
{: caption="Tabela 2. Configuração Avançada do Sistema" caption-side="top"}

 Consulte  {{site.data.keyword.cloud_notm}}  Suporte para obter informações adicionais.

 **NOTA:** é possível solicitar sub-redes secundárias com os dispositivos de cálculo. No entanto, se você
solicitar sub-redes secundárias, elas serão recuperadas quando o dispositivo de cálculo for recuperado. Se você pedir a sub-rede
secundária independentemente (não como uma opção de complemento de um pedido de cálculo), será possível reter a sub-rede até que
ela seja cancelada explicitamente. É importante lembrar dessa distinção para que nenhum endereço IP seja inadvertidamente
perdido se um dispositivo de cálculo for recuperado.

## Próximas Etapas
Após os {{site.data.keyword.baremetal_short}} serem provisionados, é possível começar a gerenciá-los. Para obter mais informações, veja [Gerenciando o {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
