---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selecionando a partir dos servidores mais populares
{: #bm-select-popular-servers}

Os servidores na lista Servidores mais populares são pré-configurados para atender às necessidades da maioria dos casos de uso dos clientes e eles estão prontos para execução de 30 a 40 minutos após o seu pedido.
1. Abra o [catálogo do {{site.data.keyword.cloud_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/catalog/){: new_window}.   
2. Selecione Bare Metal Server.
3. Clique em Continuar. Se você não vir um botão Continuar, poderá ser necessário efetuar login.
2. Na seção {{site.data.keyword.baremetal_short}}, selecione as informações a seguir:     <table>
    <CAPTION>Tabela 1. Seleções de Bare metal</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantidade</td>
    <td>Use os ícones + e - para especificar o número de servidores **idênticos** para provisão. O padrão é 1.<br>Se você desejar provisionar múltiplos servidores com especificações **diferentes**, será necessário provisioná-los separadamente.<tr>
    <tr>
    <td>Tipo de faturamento</td>
    <td>Selecione Por hora ou Mensal <tr>
    <td>Hostname e Domain</td>
    <td>Esses campos são preenchidos com o padrão. Você pode mudá-los.</td>
    </tr>
    <tr>
    <td>Localização</td>
    <td>Selecione a região na qual você deseja que o servidor seja localizado. Usando a lista suspensa, selecione um data center na região. </td>
    </tr>
    <tr>
    <tr>
    <td>Selecione o servidor</td>
    <td>Selecione **Servidores populares** e selecione o servidor que atenda às suas necessidades. Esses servidores são pré-configurados e estão prontos para uso em 30 a 40 minutos.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Padrão baseado no servidor selecionado.</td>
    </tr>
    <tr>
    <td>Chaves SSH</td>
    <td>Forneça uma chave pública da chave SSH usada para efetuar login no servidor após ele ter sido fornecido.</td>
    </tr>
    <tr>
    <td>Imagem <br>(Sistema Operacional)</td>
    <td>Selecione o sistema operacional para o servidor. Suas opções de Imagem podem ser limitadas com base no servidor selecionado.</td>
    </tr>
    <td>Complementos</td>
    <td>Expanda a seção Complementos para selecionar as opções apropriadas ou use os valores padrão./td>     </tr>
    </TBODY>
    </table>
3. Na seção Discos de armazenamento, o Disco de armazenamento já está selecionado para a seleção de seus servidores Populares. Expanda a seção Complementos se desejar incluir o IBM Cloud Backup em seu servidor.
4. Na seção Interface de rede, selecione as Velocidades da porta de uplink. Expanda a seção Complementos para selecionar as opções apropriadas ou usar os valores padrão.
4.  Revise seu pedido.
4. Se você tiver um código promocional a ser aplicado ao seu pedido, expanda Aplicar código promocional.  
5.  Revise quaisquer contratos de serviço de terceiro listados e clique na caixa de seleção **Contrato de serviço de terceiro**.
6.  Clique em  ** Provisão **. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada para o administrador: confirmação do pedido de fornecimento, aprovação e processamento do pedido de fornecimento e a conclusão do fornecimento.

 O _e-mail de fornecimento completo_ inclui um link para a página *Detalhes do dispositivo* para que você possa efetuar login no {{site.data.keyword.cloud_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.


## Próximas Etapas

Após os {{site.data.keyword.baremetal_short}} serem provisionados, é possível começar a gerenciá-los. Para obter mais informações, veja [Gerenciando o {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
