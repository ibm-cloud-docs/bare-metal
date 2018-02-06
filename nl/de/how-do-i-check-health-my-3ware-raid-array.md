---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Den Zustand Ihres 3ware-RAID-Array prüfen

Mit 3ware können Sie eine Browserschnittstelle verwenden. Wenn Sie jedoch nicht lokal auf die Schnittstelle zugreifen, kann dies ein Sicherheitsrisiko darstellen. Daher empfehlen wir, die Befehlszeilenschnittstelle zu verwenden.

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

**Schnellbefehlreferenz für 3ware-CLI-tools**

Diesen Einheiten muss eine Nummer folgen, die angibt, welche Einheit gerade abgefragt wird.

tw_cli /c0 show (Ausgabe gibt Informationen an, an denen der Zustand des RAID-Arrays ermittelt werden kann)

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

c = Controller<br/>
Controller kann 0 oder 1 sein<br/>
u = einheit<br/>
Einheitennummer hängt von der Anzahl der Arrays ab. In den meisten Fällen 0.<br/>
p = Port<br/>
Port bezeichnet die Portnummer. In den meisten Fällen 0-4.
