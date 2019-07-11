---

copyright:
  years: 1994, 2019
lastupdated: "2019-06-17"

keywords: server IP addresses, bare metal, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# IP-Adressen zuweisen und binden
{: #bm-assigning-and-binding-ip-addresses
Gehen Sie anhand der folgenden Informationen vor, um Ihrem Server eine Server-IP-Adresse zuzuweisen und bei Bedarf eine sekundäre IP-Adresse an Ihren Server zu binden.
{: shortdesc}

## Server-IP-Adressen zuweisen
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} konfiguriert Server mit den folgenden Adressen:
Eine IPv4-Adresse im privaten Netz
Eine IPv4-Adresse für den maschinennahen Managementzugriff im
privaten Netz
Eine öffentliche IPv4-Adresse, falls angefordert.

Eine IPv6-Adresse im öffentlichen Netz ist verfügbar, falls angefordert. Alle diese IP-Adressen werden gemeinsam als **primäre IP-Adressen** bezeichnet.

Weitere IP-Adressen können an Server gebunden werden, nachdem Sie **sekundäre Teilnetze** über die [{{site.data.keyword.cloud_notm}}-Konsole](https://cloud.ibm.com){: external} gekauft haben. IP-Adressen, die Sie über das Kundenportal gekauft haben und die Sie selbst verwalten, werden als **sekundäre IP-Adressen** bezeichnet.

Weitere Informationen zum Kaufen von IP-Adressen finden Sie unter [Teilnetze und IPs](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}.


## Sekundäre IP-Adressen binden
{: #bm-bind-secondary-ip-address}

Nachdem Sie ein sekundäres Teilnetz gekauft haben, müssen Sie das Betriebssystem so konfigurieren, dass es eine oder mehrere IP-Adressen verwendet. Unter jedem Betriebssystem werden IP-Adressen anders konfiguriert. Dieser Prozess wird in der Regel als Einrichten von "Aliasnamen für Schnittstellen" bezeichnet.
