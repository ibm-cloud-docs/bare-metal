---

copyright:
  years: 2018, 2019
lastupdated: "2018-04-02"

keywords: provision, sgx, provision server Intel SGX architecture, Intel SGX architecture

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Bare-Metal-Server mit Intel SGX-Architektur bereitstellen
{: #bm-server-provision-sgx}

1. Verwenden Sie die Prozedur [Angepassten Bare-Metal-Server erstellen](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Wählen Sie im Bestellformular die folgenden Optionen aus:

|Abschnitt|Auszuwählende Option|
|------|------|
|Server|Einzelprozessor,<br> Intel Xeon E3-1270 v6 mit bis zu 4 Laufwerken Speicher|
|Image|- Windows Server 2016 Standard Edition (64 Bit)<br>- Windows Server 2016 Standard Edition (64 Bit)<br> - Windows Server 2016 Datacenter Edition (64 Bit) <br>- CentOS 7.x (64 Bit) <br> - Ubuntu Linux 16.04 LTS Xenial Xerus (64 Bit)<br>- CentOS 7.x (64 Bit) <br>- Red Hat Enterprise Linux 7.x (64 Bit) (Lizenzierung pro Prozessor)|
|Image-Add-ons|Software Guard Extensions|
