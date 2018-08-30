---



copyright:
  years: 2018, 2018
lastupdated: "2018-06-18"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introdução aos Bare Metal Servers
{: #getting-started}

Os {{site.data.keyword.baremetal_long}} são servidores físicos de locatário único que fornecem desempenho e controle com
acesso de baixo nível aos recursos de hardware. O servidor não é compartilhado com "vizinhos barulhentos". Ele é todo seu!
{: shortdesc}

A Tabela 1 contém as etapas para ajudá-lo a ter rapidamente os {{site.data.keyword.baremetal_short}} fornecidos e configurados.
<table>
   <CAPTION>Tabela 1. Etapas de Inici</CAPTION>
   <THEAD>
   <TR>
   <th>Tarefa</th>
   <th>Detalhes</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. Revise o conteúdo que pode ajudar a implementação</td>
   <td>Novo no IBM Cloud e nos Bare Metal Servers? Os sites a seguir fornecem informações úteis para ajudá-lo a planejar o
ambiente.
   <li><a href="https://ibm.com/cloud-computing/"> O que é IBM Cloud </a></li>
   <li><a href="https://ibm.com/cloud/get-started">Introdução ao IBM Cloud</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Bare Metal Servers</a></li>
   </td>
 <tr>
   <td>2. Inscreva-se para o IBM Cloud</td>
   <td><a href="https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-ibm-cloud">Assinando o IBM Cloud</a> tem as
etapas sobre como configurar a conta do IBM Cloud.</td>
 <tr>
   <td>3. Determine suas especificações de carga de trabalho</td>
   <td>Antes de fornecer o servidor, determine como ele será usado e o seu tamanho necessário para obter êxito. Por exemplo, você
pretende utilizá-lo para desenvolvimento e teste ou produção? Você está testando uma experiência do usuário, processando algoritmos longos, fazendo backup e restaurando dados ou aumentando a velocidade de latência?</td>  
 <tr>
   <td>4. Dimensione e estime o custo do servidor</td>
   <td>É possível usar a <a href="https://www.ibm.com/cloud-computing/bluemix/bare-metal-search">ferramenta de procura de bare
metal</a> para ajudá-lo a dimensionar e a estimar o custo do servidor.</td>
 <tr>
   <td>5. Efetue login na conta do IBM Cloud</td>
   <td>É possível acessar o Formulário de pedido do Bare Metal Server no Catálogo do IBM Cloud ou no portal do cliente de infraestrutura do IBM Cloud. 
São necessários um <a href="https://console.bluemix.net/docs/customer-portal/getting-started.html#getting-started">IBMid e uma
senha</a> para acessar o Catálogo e o portal do cliente de infraestrutura.
   <li><a href="https://console.bluemix.net/catalog/">Catálogo do IBM Cloud</a></li>
   <li><a href="https://control.softlayer.com"> Portal do cliente de infraestrutura do IBM Cloud </a></li>  
   </td>   
<tr>   
   <td>6. Provisão de seu servidor</td>
   <td>Há três opções quando se trata de fornecer o servidor: popular, customizado e certificado pela SAP. Os servidores
populares são servidores pré-configurados que atendem às necessidades da maioria dos clientes e podem estar prontos para a
configuração de 30 a 40 minutos após o fornecimento. 
   
     
<br>Os servidores customizados são aqueles criados selecionando opções específicas de cálculo, de conectividade,
de armazenamento e de rede para atender às suas necessidades. Observe que os servidores customizados levam mais tempo para
o fornecimento, geralmente de duas a quatro horas, e têm custos operacionais mais altos. Também existe a opção de
<a href="bm_provision_ssd.html">fornecer um Bare Metal Server compatível com o Intel Optane</a> ou um com uma <a href="bare-metal-provision-SGX.html">arquitetura Intel SGX</a>. 
     
<br>Os servidores certificados pela SAP foram especificamente certificados para suportar as paisagens SAP HANA e SAP NetWeaver.
Use os links a serem considerados para fornecer informações para esse tipo de servidor. Observe que com os servidores certificados pela SAP, é necessário selecionar qual o tipo de paisagem fornecida: SAP HANA ou SAP NetWeaver.  
  <li><a href="baremetal-provision-popular.html"> Servidores Fast-provisioned bare metal </a></li>
  <li><a href="baremetal-provision.html"> Servidores bare metal customizados </a></li>
  <li><a href="bare-metal-sap-applications.html"> IBM Cloud SAP-Infra-estrutura Certificada </a></li>
  </td>
 <tr>
   <td>7. Configure seu servidor bare metal</td>
   <td>Agora, o servidor está pronto para ser configurado. Consulte os tópicos em  * Configurando *.</td>
   </td>
   </tr>
   </TBODY>
   </table>
