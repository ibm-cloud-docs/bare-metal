---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisionando o servidor bare metal

## Antes de Come╬ar
Você tem duas opções para provisionar {{site.data.keyword.baremetal_long}} públicos. O primeiro é por meio do catálogo do {{site.data.keyword.cloud}} e o segundo é por meio do {{site.data.keyword.slportal_full}}. O catálogo e o {{site.data.keyword.slportal}} requerem IDs de login exclusivos. Seu nome do usuário e senha do catálogo não funcionarão para efetuar login no portal e vice-versa.
{:shortdesc}

Antes de iniciar, assegure-se de que você tenha suas credenciais do catálogo do {{site.data.keyword.cloud_notm}} ou do {{site.data.keyword.slportal}} configuradas. 
  
**Nota:** para o catálogo do {{site.data.keyword.cloud_notm}}, deve-se ter uma conta com upgrade para pedir {{site.data.keyword.baremetal_short}}. Para obter mais informações sobre como fazer upgrade de sua conta, veja [Alternando para IBMid](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
## Efetuando login 
Certifique-se de que você tenha efetuado login por meio do catálogo do {{site.data.keyword.cloud_notm}} ou do {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Tabela 1. Escolher um log no local</CAPTION>
   <THEAD>
   <TR>
   <th>Se você deseja efetuar login com...</th>
   <th>Então...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catálogo do IBM Cloud</td>
   <td>
   <ol>
   <li>Abra uma nova janela do navegador e insira <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Clique no link <b>Efetuar login</b>. </li>
   <li>Insira seu e-mail ou IBMid e clique em <b>Continuar</b>.</li>
   <li>Insira sua senha e clique em <b>Efetuar login</b>.</li>
   <li>Selecione <b>Infraestrutura</b> > <b>Cálculo</b>.</li>
   <li>Clique no quadro <b>{{site.data.keyword.baremetal_short}}</b>.</li>
   <li>Clique em <b>Criar</b>. A página principal do {{site.data.keyword.slportal}} é aberta.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portal do Cliente</td>
   <td>
   <ol>
   <li>Abra uma nova janela do navegador e insira <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Insira seu Nome do usuário e Senha e clique em <b>Efetuar login</b>. Ou clique em <b>Efetuar login com o IBMid</b>. Em seguida, insira seu e-mail ou IBMid e clique em <b>Continuar</b>. Insira sua senha e clique em <b>Efetuar login</b>. A página principal do {{site.data.keyword.slportal}} é aberta.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisionando um servidor bare metal
{: #ordering-baremetal-server}
Depois de ter efetuado login, é possível começar a provisionar os {{site.data.keyword.baremetal_short}}. É possível provisionar os {{site.data.keyword.baremetal_short}} por meio do menu **Dispositivos** ou do ícone **Dispositivos**.

### Provisionando um servidor bare metal por meio do ícone Dispositivos
Para provisionar os {{site.data.keyword.baremetal_short}} por meio do ícone *Dispositivos*, conclua as etapas a seguir:

1.  No {{site.data.keyword.slportal}}, localize a seção **Pedido** e clique em **Dispositivos**.
2.  Na página Dispositivos, clique em **Por hora** ou **Mensal** em {{site.data.keyword.baremetal_short}}.
3.  Selecione o seu **Data Center**, role pela página e clique no link **Iniciando preço por** para selecionar o seu servidor. 
4.  Preencha as informações na página **Configure o seu {{site.data.keyword.baremetal_short}}** e clique no botão **Incluir na ordem** para continuar. Veja [Configurando o seu {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md) para obter mais informações sobre como configurar o seu servidor. Logo que a sua ordem for verificada, você será redirecionado para a página de **Check-out**.
5.  Insira a **Configuração do sistema avançado** para o servidor. Veja [Configurando o seu {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md) para obter mais informações sobre como configurar isso.
6.  Clique nas caixas de seleção **termos do Cloud Service** e **Contrato de prestação de serviços de terceiro**.
7.  Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

 Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento inclui um link para sua página *Detalhes do dispositivo*, depois de efetuar login no {{site.data.keyword.cloud_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

### Provisionando o servidor bare metal por meio do menu Dispositivos
{: #ordering-baremetal-devices-menu}

Também é possível provisionar {{site.data.keyword.baremetal_short}} por meio do menu *Dispositivos* na página principal do {{site.data.keyword.slportal}}. 

1. Clique em **Dispositivos > Lista de dispositivos**. A página Dispositivos exibe todos os tipos de dispositivo — hosts dedicados, servidores virtuais, servidores bare metal e controladores de entrega de aplicativo NetScaler - em sua conta.
2. Clique no link **Pedir dispositivos** no canto superior direito.
3. Na página Pedir produtos e serviços SoftLayer, clique em **Por hora** ou **Mensal** em {{site.data.keyword.baremetal_short}}.
4. Selecione o seu **Data Center**, role pela página e clique no link **Iniciando preço por** para selecionar o seu servidor. 
5.  Preencha as informações na página **Configure o seu {{site.data.keyword.baremetal_short}}** e clique no botão **Incluir na ordem** para continuar. Veja [Configurando o seu {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md) para obter mais informações sobre como configurar o seu servidor. Logo que a sua ordem for verificada, você será redirecionado para a página de **Check-out**.
6.  Insira a **Configuração do sistema avançado** para o servidor. Veja [Configurando o seu {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md) para obter mais informações sobre como configurar isso.
7. Clique nas caixas de seleção **termos do Cloud Service** e **Contrato de prestação de serviços de terceiro**.
8. Confirme ou insira suas informações de pagamento e clique no botão **Enviar ordem**. Você é redirecionado para uma tela com seu número de ordem de fornecimento. É possível imprimir a tela porque ela também é seu recibo de ordem de fornecimento.

Uma série de e-mails é enviada a seu administrador: confirmação, aprovação e processamento da ordem de fornecimento, e fornecimento concluído. O e-mail completo de fornecimento inclui um link para sua página *Detalhes do dispositivo*, depois de efetuar login no {{site.data.keyword.cloud_notm}}. Também é possível registrar-se diretamente no {{site.data.keyword.slportal}}.

### Próximas Etapas
Após os {{site.data.keyword.baremetal_short}} serem provisionados, é possível começar a gerenciá-los. Para obter mais informações, veja [Gerenciando o {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
