---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Controllo dello stato del tuo array RAID 3ware

Con 3ware, puoi utilizzare un'interfaccia browser. Tuttavia, a meno che tu non acceda all'interfaccia localmente, può rappresentare un rischio per la sicurezza. Utilizzi pertanto l'interfaccia riga di comando (CLI).

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

**Guida di riferimento rapida ai comandi per gli strumenti della CLI 3ware**

Questi dispositivi devono essere seguiti da un numero che identifica quali di essi siano attualmente oggetto della query.

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
Il valore port denota il numero di porta. Nella maggior parte dei casi, è 0-4.
