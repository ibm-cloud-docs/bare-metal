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

# Den Zustand Ihres 3ware-RAID-Array prüfen
{: #bm-check-health-3ware-raid}

Mit 3ware können Sie eine Browserschnittstelle verwenden. Wenn Sie jedoch nicht lokal auf die Schnittstelle zugreifen, kann dies ein Sicherheitsrisiko darstellen. Daher sollten Sie die Befehlszeilenschnittstelle verwenden.

Sie können die 3ware-CLI-Dienstprogramme aus dem [IBM Cloud-CLI-Plug-in-Repository
](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins) herunterladen. Weitere Informationen zum CLI-Dienstprogramm finden Sie unter [VPN-CLI-Plug-in für die Befehlszeilenschnittstelle 'cf'](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf).

**Kurzbefehlsreferenz für 3ware-CLI-Tools**

Diesen Einheiten muss eine Nummer folgen, die angibt, welche Einheit abgefragt wird.

tw_cli /c0 show (Ausgabe enthält Informationen, mit denen der Zustand des RAID-Arrays ermittelt werden kann)

./tw_cli /c1 show

Beispiel:

    Einheit  Einheitentyp  Status         %Cmpl  Stripegröße (GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*Hinweis:

c = controller<br/>
Controller kann 0 oder 1 sein<br/>
u = unit<br/>
Einheitennummer hängt von der Anzahl der Arrays ab. In den meisten Fällen 0.<br/>
p = port<br/>
Port bezeichnet die Portnummer. In den meisten Fällen 0-4.
