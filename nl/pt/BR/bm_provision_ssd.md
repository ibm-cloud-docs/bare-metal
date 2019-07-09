---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Fornecendo um Bare Metal Server compatível com o Intel Optane
{: #bm-provision-optane-server}

Para fornecer um Bare Metal Server com uma unidade Intel Optane:
1. Use o procedimento: [Construindo um Bare Metal Server customizado](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Selecione as opções a seguir no formulário do pedido:

|Seção|Opção para selecionar
|------|------|
|Região-Data Center|Para usar a unidade Intel Optane, selecione um dos seguintes data centers:<br>Europa - AMS03, FRA02, LON02, OSL01<br>NA Sul DAL09, DAL10, DAL12<br>Ásia-Pacífico - MEL01<br>NA Leste - MON01, TOR01, WDC04<br>NA Oeste - SJC03<br>|
|Servidor|1. Selecione **Todos os servidores**<br>2. Selecione *Processadores dual*<br>3. Selecione um dos servidores a seguir<br>-Intel Xeon 4110, até 12 unidades<br>-Intel Xeon 5120 com até 12 unidades<br>-Intel Xeon 6140 com até 12 unidades<br>-Intel Xeon E5-2620 v4 com suporte GPU<br>-Intel Xeon E5-2650 v4 com suporte GPU<br>-Intel Xeon E5-2690 v4 com suporte GPU<br><br>  **Nota**: se você selecionar E5-2620 v4, E5-2650 v4 ou E5-2650 v4, a unidade Intel Optane substituirá a GPU, portanto, não será possível ter uma GPU e uma unidade Intel Optane.|
|Sistema Operacional|Para drivers Optane fornecidos pela Intel, os seguintes sistemas operacionais são certificados pela Intel:<br>Windows Server 2016 (todas as Edições)<br>Windows Server 2012 R2 (todas as Edições)<br><br>Para drivers não Intel, nativos e de software livre, a compatibilidade e a funcionalidade são validadas, mas não certificadas:<br>Red Hat Enterprise Linux 7.x (64 bits)<br>Red Hat Enterprise Linux 6.x (64 bits).
|Complementos de imagem| Selecione uma unidade Intel Optane para o primeiro e o segundo componentes PCIe ou para ambos.|
