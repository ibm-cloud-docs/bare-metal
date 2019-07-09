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

# Provisioning di un server bare metal con l'architettura Intel SGX
{: #bm-server-provision-sgx}

1. Utilizza la procedura: [Creazione di un server bare metal personalizzato](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Seleziona le seguenti opzioni sul modulo d'ordine:

|Sezione|Opzione da selezionare|
|------|------|
|Server|Singolo processore,<br> Intel Xeon E3-1270 v6 con memoria fino a 4 unità |
|Immagine |- Windows Server 2016 Standard Edition (64 bit)<br>- Windows Server 2016 Standard Edition (64 bit)<br> - Windows Server 2016 Datacenter Edition (64 bit) <br>- CentOS 7.x (64 bit) <br> - Ubuntu Linux 16.04 LTS Xenial Xerus (64 bit)<br>- CentOS 7.x (64 bit) <br>- Red Hat Enterprise Linux 7.x (64 bit) (licenze per processore)|
|Componenti aggiuntivi immagine |SGX (Software Guard Extensions)|
