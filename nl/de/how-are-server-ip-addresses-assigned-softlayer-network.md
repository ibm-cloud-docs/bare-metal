---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Server-IP-Adressen zuweisen

{{site.data.keyword.cloud}} konfiguriert Server mit einer IPv4-Adresse im privaten Netz, einer IPv4-Adresse für den maschinennahen Managementzugriff im privaten Netz und, falls angefordert, einer öffentlichen IPv4-Adresse.
Eine IPv6-Adresse im öffentlichen Netz ist verfügbar, falls angefordert. Alle diese IP-Adressen werden gemeinsam als **primäre IP-Adressen** bezeichnet. 

Weitere IP-Adressen können an Server gebunden werden, nachdem Sie **sekundäre Teilnetze** über das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com) gekauft haben. IP-Adressen, die Sie über das Kundenportal gekauft haben und die Sie selbst verwalten, werden als **sekundäre IP-Adressen** bezeichnet. 

Weitere Informationen zum Kaufen von IP-Adressen finden Sie unter [Teilnetze und IPs](https://console.bluemix.net/docs/infrastructure/subnets/). 


# Sekundäre IP-Adressen binden

Nachdem Sie ein sekundäres Teilnetz gekauft haben, müssen Sie das Betriebssystem so konfigurieren, dass es eine oder mehrere IP-Adressen verwendet. Unter jedem Betriebssystem werden IP-Adressen anders konfiguriert. Dieser Prozess wird in der Regel als Einrichten von "Aliasnamen für Schnittstellen" bezeichnet.  
