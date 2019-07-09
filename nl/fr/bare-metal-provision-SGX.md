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

# Mise à disposition d'un serveur bare metal avec l'architecture Intel SGX
{: #bm-server-provision-sgx}

1. Utilisez la procédure [Génération d'un serveur bare metal personnalisé](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Sélectionnez les options suivantes du formulaire de commande :

|Section|Option à sélectionner|
|------|------|
|Serveur|Processeur unique,<br> Intel Xeon E3-1270 v6 avec un stockage de jusqu'à 4 unités |
|Image|- Windows Server 2016 Standard Edition (64 bits)<br>- Windows Server 2016 Standard Edition (64 bits)<br> - Windows Server 2016 Datacenter Edition (64 bits) <br>- CentOS 7.x (64 bits) <br> - Ubuntu Linux 16.04 LTS Xenial Xerus (64 bits)<br>- CentOS 7.x (64 bits) <br>- Red Hat Enterprise Linux 7.x (64 bits) (licence par processeur)|
|Modules complémentaires d'image|Software Guard Extensions|
