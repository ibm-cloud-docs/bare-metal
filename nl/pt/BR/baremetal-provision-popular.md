---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selecionando a partir dos servidores mais populares
Os servidores na lista Servidores mais populares são pré-configurados para atender às necessidades da maioria dos casos de
uso dos clientes e eles estão prontos para execução de 30 a 40 minutos após o seu pedido.
1. Abra o  [ {{site.data.keyword.cloud_notm}}  catálogo ](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Selecione Bare Metal Server.
3. Clique em Criar.
2. Selecione as seguintes informações:
    <table>
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
    <td>Use os ícones + e - para especificar o número de servidores idênticos para o fornecimento. <br>Se desejar fornecer
múltiplos servidores com diferentes especificações, será necessário fornecê-los separadamente.
    <tr>
    <td>Localização</td>
    <td>Selecione a região e o data center em que deseja que o servidor seja localizado.</td>
    </tr>
    <tr>
    <tr>
    <td>Hostname e Domain</td>
    <td>Esses campos são preenchidos com o padrão. Você pode mudá-los.</td>
    </tr>
    <tr>
    <td>Selecione o servidor</td>
    <td>Em **Servidores populares**, selecione o servidor que atende às suas necessidades. Esses servidores são
pré-configurados e estão prontos para uso em 30 a 40 minutos.
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
    <td>Selecione o sistema operacional para a instância. **Nota**: uma mensagem de erro será exibida se existir um conflito entre o servidor e o sistema operacional. Por exemplo, selecionar Linux em um Microsoft SQL server.</td>
    </tr>
    <td>Velocidades da Porta de Uplink</td>
    <td>Determina a velocidade de interfaces internas e externas.</td>
    </tr>
    <tr>
    <td>Complementos</td>
    <td> Selecione as opções apropriadas ou use os valores padrão.</td>
    </tr>
    </TBODY>
    </table>

3.  Na seção Resumo do pedido, selecione o faturamento **Por hora** ou o **Mensal**.
4.  Revise seu pedido.
5.  Revise quaisquer contratos de serviço de terceiro listados e clique na caixa de seleção **Contrato de serviço de
terceiro**.
6.  Clique em  ** Provisão **. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada para o administrador: confirmação do pedido de fornecimento, aprovação e
processamento do pedido de fornecimento e a conclusão do fornecimento. O e-mail completo de fornecimento inclui um link para a
página *Detalhes do dispositivo* para que você possa efetuar login no {{site.data.keyword.cloud_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.


## Próximas Etapas
Após os {{site.data.keyword.baremetal_short}} serem provisionados, é possível começar a gerenciá-los. Para obter mais informações, veja [Gerenciando o {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
