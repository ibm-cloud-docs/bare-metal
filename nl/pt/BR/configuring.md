---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurando seu servidor bare metal

É uma boa ideia reservar um tempo e tomar suas decisões de configuração antes de provisionar seus {{site.data.keyword.baremetal_long}}. Isso torna o processo de fornecimento mais rápido e fácil. {:shortdesc}

## Determinando o uso do servidor e dimensionando-o

Sua primeira tarefa é determinar como você usará seus {{site.data.keyword.baremetal_short}}. Por exemplo, você pretende usá-lo para des./teste ou produção? Você está testando uma experiência do usuário, processando algoritmos longos, fazendo backup e restaurando dados ou aumentando a velocidade de latência?

Após determinar como seus {{site.data.keyword.baremetal_short}} devem ser usados, você precisa dimensioná-los. A [Calculadora de custo total de propriedade do SoftLayer](http://www.softlayer.com/tco/) pode ajudar a determinar o que nos {{site.data.keyword.baremetal_short}} atende melhor às suas necessidades.

## Selecionando seu servidor

O {{site.data.keyword.cloud_notm}} oferece sete servidores de provisão rápida para assegurar que você tenha o desempenho necessário para sua carga de trabalho. Esses servidores estão atualmente disponíveis nas regiões Reino Unido e Sul dos EUA.

| **Configuração** | **Processador** | **Memória** | **Disco rígido** | **Velocidade da porta** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 núcleos, 3,50 GHz) |RAM de 32 GB |1 unidade interna de disco rígido |velocidade da porta máxima de 100 Mbps|
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3 (6 núcleos, 2.40 GHz) |RAM de 64 GB |2 unidades internas de disco rígido |velocidade da porta máxima de 100 Mbps|
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 núcleos, 3,50 GHz) |RAM de 32 GB |2 unidades internas de disco rígido |velocidade da porta máxima de 100 Mbps|
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3 (10 núcleos, 2,30 GHz) |RAM de 128 GB |1 unidade interna de disco rígido |velocidade da porta máxima de 100 Mbps|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 núcleos, 2,60 GHz) |RAM de 128 GB |2 unidades internas de disco rígido |velocidade da porta máxima de 100 Mbps|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 núcleos, 2,60 GHz) |RAM de 64 GB |4 unidades internas de disco rígido |velocidade da porta máxima de 1.000 Mbps|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 núcleos, 2,60 GHz) |RAM de 256 GB |4 unidades internas de disco rígido |velocidade da porta máxima de 1.000 Mbps|

Além dos sete servidores de provisão rápida, o {{site.data.keyword.cloud_notm}} expandiu sua oferta de {{site.data.keyword.baremetal_short}} para incluir sistemas bare metal baseados no POWER8. Esses sistemas são construídos com o processador {{site.data.keyword.IBM_notm}} POWER8 e uma plataforma baseada no OpenPOWER, que é ajustada especificamente para implementações baseadas em nuvem de dados, cognitiva e de carga de trabalho da web no Linux.

Qualquer um dos {{site.data.keyword.baremetal_short}} pode ser submetido a upgrade para incluir a largura da banda não medida (ilimitada). Todos os dispositivos não medidos estão em portas privadas, dedicadas.

## Configurando seus servidores bare metal

Depois de selecionar o data center, servidor e opção de faturamento (mensal ou por hora), você precisa decidir como configurar o servidor. Alguns campos (Servidor, RAM, Unidade de Processamento de Gráfico e Unidade de Processamento de Gráfico Secundário) na página **Configurar {{site.data.keyword.baremetal_short}}** serão padrão com base em sua seleção do servidor. A tabela a seguir descreve os campos para os quais é possível definir um valor.

| **Campo** | **Descrição** |
|-------------------|---------------|
|Sistema operacional |Selecione entre CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu ou Outro. |
|Discos rígidos |A ferramenta Disk Configuration ajuda a configurar seus discos rígidos preenchendo os campos com base em sua seleção do S.O. |
|Largura da Banda Pública |Determina a quantia de dados que podem ser transferidos por meio da interface pública durante um mês. Para ambientes de teste, que precisam que os dados de instalação sejam transferidos por meio dessa interface, os valores precisam ser adaptados além da quantia de dados transferidos inicialmente. Você pode desejar considerar o [{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) para enviar um carregamento de dados iniciais para um dos data centers do {{site.data.keyword.cloud_notm}}. |
|Velocidades da Porta de Uplink |Determina a velocidade de interfaces internas e externas. |
|Endereços IP secundários públicos |Designa um endereço IP adicional para seu servidor. Dependendo de seu cenário, você pode requerer mais endereços IP designados para seu servidor. Endereços IPv4 adicionais estão disponíveis em quantidades 1, 2, 4, 8, 16 ou 32. |
|Endereços IPv6 primários |Designado às interfaces internas e externas do servidor. |
|Endereços IPv6 estáticos públicos |Designa endereços IPv6 adicionais de um bloco /64. |
|Firewalls de & hardware e software, &  antivírus e proteção contra spyware, intrusão e detecção & e proteção |Selecione as opções apropriadas se o servidor será voltado para a Internet. É altamente recomendado alinhar seu departamento de segurança corporativa com o Suporte do {{site.data.keyword.cloud_notm}} para discutir os detalhes dessas opções. |
|Evault |Uma ferramenta de backup baseado em agente que pode ser instalada em seu servidor para replicar backups entre servidores. |

Consulte o Suporte do {{site.data.keyword.cloud_notm}} para obter informações adicionais.


## Configuração do sistema avançado

A configuração do sistema avançado é feita depois que você clica no botão **Incluir na ordem** e é redirecionado para a página Check-out. A tabela a seguir descreve os campos sob Configuração do sistema avançado.

| **Campo** | **Descrição** |
|-------------------|---------------|
|Nome do host |Um nome permanente ou provisório para seu servidor, por exemplo, _server1_. |
|Domínio |O nome de subdomínio que não deve ser conflitante com um nome do domínio da Internet, por exemplo, _test.acme.com_. |
|Seleção de VLAN |Se houver uma VLAN sob sua conta porque você já pediu pelo menos um servidor, será possível incluir o novo servidor nessa VLAN. |
|Script de fornecimento |É possível fornecer um script que permite automatizar determinadas etapas após o servidor ter sido provisionado. |
|Chaves SSH |É possível fornecer uma chave pública para sua chave SSH, que permitirá efetuar login em seu servidor após ele ser provisionado. |
