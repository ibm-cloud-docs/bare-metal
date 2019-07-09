---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-25"

keywords: bare metal, 3ware 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Controllo dello stato del tuo array RAID 3ware
{: #bm-check-health-3ware-raid}

Con 3ware, puoi utilizzare un'interfaccia del browser. Tuttavia, a meno che tu non acceda all'interfaccia localmente, può rappresentare un rischio per la sicurezza. Pertanto, utilizzi l'interfaccia della riga di comando.

Puoi scaricare i programmi di utilità della CLI 3ware da [Repository di plugin CLI IBM Cloud
](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins). Per ulteriori informazioni sul programma di utilità della CLI, vedi [Plug-in CLI VPN per la CLI cf](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf).

**Guida di riferimento rapida ai comandi per gli strumenti della CLI 3ware**

Questi dispositivi devono essere seguiti da un numero che identifica il dispositivo su cui viene eseguita la query.

tw_cli /c0 show (l'output mostra le informazioni necessarie per conoscere lo stato dell'array RAID)

./tw_cli /c1 show

Esempio:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*nota quanto segue:

c = controller<br/>
Il controller può essere 0 o 1<br/>
u = unit<br/>
Il numero di unità dipende dagli array di numeri. È 0 nella maggior parte dei casi.<br/>
p = port<br/>
Port indica il numero di porta. Nella maggior parte dei casi, è 0-4.
