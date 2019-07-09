---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-19"

keywords: bare metal, bare metal servers, POWER8, SAP-certified, {{site.data.keyword.baremetal_long}}, {{site.data.keyword.baremetal_short}}, available bare metal, cascade lake

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}

# Sobre servidores bare metal
{: #about-bm}

Os {{site.data.keyword.baremetal_long}} são a base para a solução de infraestrutura como serviço. Se você é um
desenvolvedor de jogos que requer E/S de alta velocidade ou precisa de servidores de alto desempenho para os usuários, os
{{site.data.keyword.baremetal_short}} podem atender às suas necessidades de computação.
{:shortdesc}

Os {{site.data.keyword.baremetal_short}} são servidores de locatário único, por hora ou mensal, dedicados a você;
nenhuma parte deles, incluindo os recursos do servidor, é compartilhada com os outros clientes. Você gerencia seu servidor, que é provisionado sem um hypervisor, e implementado em um ou mais data centers. Múltiplos {{site.data.keyword.baremetal_short}} podem se comunicar na rede privada virtual do {{site.data.keyword.cloud_notm}}
como se estivessem dispostos no mesmo rack.

## Servidores para cada carga de trabalho
{: #servers-every-need}

{{site.data.keyword.cloud_notm}}  tem  {{site.data.keyword.baremetal_short}}  para ajustar cada carga de trabalho. Para
obter mais informações, consulte
[Servidores bare metal](https://www.ibm.com/cloud/bare-metal-servers){: external}

### Servidores de provisionamento rápido
{: #Popular-bm}

O {{site.data.keyword.cloud_notm}} oferece servidores pré-configurados que atendem às necessidades da maioria dos
casos de uso. Esses servidores são considerados de "fornecimento rápido", pois as suas opções de cálculo (o número de
núcleos, a velocidade, a RAM e o número de unidades) são pré-configuradas. Os servidores pré-configurados estão prontos para
a configuração de 30 a 40 minutos após o fornecimento. 

### Servidores baseados em customização
{: #custom-based-bm}

Se um dos servidores de fornecimento rápido não atender às suas necessidades de
carga de trabalho, será possível customizar seu
{{site.data.keyword.baremetal_short}} para atender às suas necessidades. Os servidores customizados são fornecidos em duas a quatro horas e oferecem uma maior variedade de núcleos, de velocidades, de RAM
e de unidades. 

### Servidores baseados em POWER8 customizados
{: #bm-power8}

O {{site.data.keyword.cloud_notm}} oferece a opção de fornecer um Bare Metal Server baseado no IBM POWER8. Os
servidores POWER8 são desenvolvidos com o processador POWER8 e uma plataforma baseada em OpenPower que é ajustada
especificamente para as implementações baseadas em nuvem para os dados, os cognitivos e as cargas de trabalho da web no Linux. Para obter mais informações, consulte [Servidores POWER8](https://www.ibm.com/cloud/bare-metal-servers/power){: external}.

### Servidores bare metal certificados por SAP
{: #bm-SAP-cert}

Os {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} são certificados para suportar as
cargas de trabalho do SAP HANA e do SAP NetWeaver. Para obter mais informações, consulte
[Infraestrutura certificada pelo SAP](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

## Opções disponíveis para servidores bare metal <!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
O {{site.data.keyword.cloud_notm}} tem opções do
{{site.data.keyword.baremetal_short}} que podem ser customizadas para atender às
suas necessidades.

### Suporte ao Intel Cascade Lake CPU
<!--Need to add which servers are also available for SAP once the certification is done-->
Agora é possível escolher entre as CPUs Intel Cascade Lake a seguir quando você provisiona um servidor bare metal:

* Intel Xeon 4210 (10-Core, 2.2 GHz, 85 W)
* Intel Xeon 5218 (16-Core, 2.3 GHz, 125 W)
* Intel Xeon 6248 (20-Core, 2.6 GHz, 150 W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Os processadores Cascade Lake estão disponíveis nos data centers a seguir:

<table style="width:100%">
<CAPTION>Tabela 1. Data centers com processadores Cascade Lake</CAPTION>
 <tr>
   
   <th colspan="6">Datacenters</th>
 </tr>
 <tr>
   <td>DAL10</td>
   <td>FRA02</td>
   <td>LON04</td>
   <td>SYD01</td>
   <td>TOK02</td>
   <td>WDC04</td>
   
</tr>

<tr>
  <td>DAL12</td>
  <td>FRA04</td>
  <td>LON05</td>
  <td>SYD04</td>
  <td>TOK04</td>
  <td>WDC06</td>
  
</tr>

<tr>
  <td>DAL13</td>
  <td>FRA05</td>
  <td>LON06</td>
  <td>SYD05</td>
  <td>TOK05</td>
  <td>WDC07</td>
</tr>
</table>


### Inventário dinâmico
{: #bm-dynamic-inv}

Agora é possível ver quais servidores estão disponíveis em qual centro de dados
quando você provisiona um servidor bare metal. Mas essa opção está disponível somente
para a oferta horária. Não é possível ver a disponibilidade do servidor com a oferta
mensal. Para obter mais informações sobre o fornecimento de um servidor bare metal,
consulte [Selecionando
entre servidores de fornecimento rápido](/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Complemento de armazenamento de bloco e arquivo
{: #bm-block-and-file-add-on}

Se você precisar de armazenamento extra, o
{{site.data.keyword.IBM_notm}} facilita isso! Agora é possível solicitar
armazenamento de bloco e de arquivo (20 - 12.000 GB) quando você provisiona um servidor
bare metal. 

Seu armazenamento de complemento não está conectado automaticamente ao seu servidor
bare metal. É preciso conectar o armazenamento de complemento ao servidor bare metal
após as provisões do servidor.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

Para obter mais informações sobre o armazenamento de bloco e de arquivo, consulte os links a seguir.
* [Sobre o armazenamento de bloco](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [Sobre o armazenamento de arquivo](/docs/infrastructure/FileStorage?topic=FileStorage-about)
