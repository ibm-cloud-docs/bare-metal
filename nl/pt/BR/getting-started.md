---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-16"

keywords: bare metal, getting started, {{site.data.keyword.cloud}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Tutorial Introdução
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
   <td><a href="https://cloud.ibm.com/docs/account?topic=account-signup#signing-up-for-ibm-cloud">Assinando o IBM Cloud</a> tem as
etapas sobre como configurar a conta do IBM Cloud.</td>
 <tr>
   <td>3. Determine suas especificações de carga de trabalho</td>
   <td>Antes de provisionar seu servidor, determine como ele será usado e o tamanho do
servidor que você precisa para ser bem-sucedido. Por exemplo, você
pretende utilizá-lo para desenvolvimento e teste ou produção? Você está testando uma experiência do usuário, processando algoritmos longos, fazendo backup e restaurando dados ou aumentando a velocidade de latência?</td>  
 <tr>
   <td>4. Dimensione e estime o custo do servidor</td>
   <td>É possível usar a <a href="https://cloud.ibm.com/gen1/infrastructure/provision/bm">ferramenta de procura de bare
metal</a> para ajudá-lo a dimensionar e a estimar o custo do servidor.</td>
 <tr>
   <td>5. Efetue login na conta do IBM Cloud</td>
   <td>É possível acessar o Formulário de pedido do Bare Metal Server no Catálogo do IBM Cloud ou no portal do cliente de infraestrutura do IBM Cloud. São necessários um <a href="https://cloud.ibm.com/docs/customer-portal?topic=customer-portal-getting-started#getting-started">IBMid e uma
senha</a> para acessar o Catálogo e o portal do cliente de infraestrutura.
   <li><a href="https://cloud.ibm.com/catalog/">Catálogo do IBM Cloud</a></li>
   <li><a href="https://cloud.ibm.com">Console do IBM Cloud</a></li>  
   </td>   
<tr>   
   <td>6. Provisão de seu servidor</td>
   <td>Você tem três opções quando se trata de provisionar seu servidor:
fornecimento rápido, customizado e certificado SAP. Os servidores de fornecimento rápido
são servidores pré-configurados que atendem às necessidades da maioria dos clientes e
podem estar prontos para configuração 30 a 40 minutos após o fornecimento.


<br>Servidores customizados são servidores que você cria selecionando opções de
cálculo, conectividade, armazenamento e rede específicas para atender às suas
necessidades. Os servidores customizados levam mais tempo para serem provisionados, geralmente de
2 a 4 horas, e têm custos operacionais mais altos. É possível
[Provisionar
um servidor bare metal compatível com Intel Optane](/docs/bare-metal?topic=bare-metal-provisioning-an-intel-optane-compatible-bare-metal-server#provisioning-an-intel-optane-compatible-bare-metal-server) ou um com uma
[arquitetura
Intel SGX](/docs/bare-metal?topic=bare-metal-provisioning-a-bare-metal-server-with-intel-sgx-architecture#provisioning-a-bare-metal-server-with-intel-sgx-architecture).

<br>Os servidores certificados SAP são certificados para suportar as paisagens
SAP HANA e SAP NetWeaver.Use os links a serem considerados para fornecer informações para esse tipo de servidor. Observe
que, com servidores certificados SAP, é necessário selecionar qual tipo de
paisagem, SAP HANA ou SAP NetWeaver, você está provisionando.<br>
* [ Servidores Fast-provisioned bare metal ](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers)<br>
* [ Servidores bare metal customizados ](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server#ordering-baremetal-server)<br>
* [IBM Cloud SAP-Infra-estrutura Certificada](/docs/bare-metal?topic=bare-metal-ibm-cloud-sap-certified-infrastructure#ibm-cloud-sap-certified-infrastructure)
  </td>
 <tr>
   <td>7. Configure seu servidor bare metal</td>
   <td>Agora, o servidor está pronto para ser configurado. Consulte os tópicos em  ** Configurando **.</td>
   </td>
   </tr>
   </TBODY>
   </table>
