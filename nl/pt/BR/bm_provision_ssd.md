---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Fornecendo um Bare Metal Server compatível com o Intel Optane
Para fornecer um Bare Metal Server com uma unidade Intel Optane:
1. Use o procedimento: [Construindo um Bare Metal Server customizado](../bare-metal/baremetal-provision.html).
* Selecione as opções a seguir no formulário do pedido:

|Seção|Opção para selecionar
|------|------|
|Datacenter|Para usar a unidade Intel Optane, selecione um dos seguintes data centers:<br>AMS03-Amsterdã<br>DAL09-Dallas<br>DAL10-Dallas<br>DAL12-Dallas<br>FRA02-Frankfurt<br>LON02-Londres<br>MEL01-Melbourne<br>
MON01 - Montreal<br>OSL01-Oslo<br>SJC03-San Jose<br>TOR01-Toronto<br>WDC04-Washington, DC|
|Servidor|Os servidores a seguir são compatíveis com a unidade Intel Optane<br>Intel Xeon 4110 com até 12 unidades<br>Intel Xeon 5120 com até 12 unidades<br>
Intel Xeon 6140 com até 12 unidades<br>Intel Xeon E5-2620 v4 com suporte à GPU<br>Intel Xeon E5-2650 v4 com suporte à GPU<br>Intel
Xeon E5-2690 v4 com suporte à GPU<br><br>  **Nota**: se você selecionar E5-2620 v4, E5-2650 v4 ou E5-2650 v4, a
unidade Intel Optane substituirá a GPU, portanto, não será possível ter uma GPU e uma unidade Intel Optane.|
|Componentes PCIe|Selecione uma unidade Intel Optane para o primeiro e o segundo componentes PCIe ou para ambos.|
|Sistema Operacional|Para drivers Optane fornecidos pela Intel, os seguintes sistemas operacionais são certificados pela Intel:<br>Windows Server 2016 (todas as Edições)<br>Windows Server 2012 R2 (todas as Edições)<br><br>
Para drivers não Intel, nativos e de software livre, a compatibilidade e a funcionalidade são validadas, mas não certificadas:<br>Red
Hat Enterprise Linux 7.x (64 bits)<br>Red Hat Enterprise Linux 6.x (64 bits).
