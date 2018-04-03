---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Backup e ripristino

{{site.data.keyword.Bluemix_notm}} fornisce diverse [soluzioni di backup e archiviazione](https://www.softlayer.com/cloud-storage) scalabili per soddisfare i tuoi requisiti di backup. Tuttavia, non completiamo i backup dei dispositivi dei clienti. Un utente sul tuo account deve avviare tutti i backup pianificati e una tantum sui tuoi dispositivi.

Se su un account esistono due o più {{site.data.keyword.baremetal_short}}, è possibile eseguire il backup da un dispositivo a un altro. Non c'è alcun limite di larghezza di banda per il traffico di rete privata e, pertanto, è possibile eseguire il trasferimento o il backup dei dati tra qualsiasi dispositivo che condivide un account in qualsiasi momento.
Sono disponibili diverse soluzioni di backup per {{site.data.keyword.baremetal_short}}, comprese le seguenti:

1. [Evault Backup](/infrastructure/backup/index.html) è una soluzione di backup aziendale che può automatizzare i backup su più server. I dati vengono memorizzati in una SAN (storage area network) aziendale.
* [NAS (Network Attached Storage)](/infrastructure/network-attached-storage/nas.html) è uno standard del settore e fornisce memorizzazione esterna al server per i dati critici. I dati vengono memorizzati in una SAN (storage area network) aziendale.
* [R1Soft CDP](/infrastructure/backup/r1soft.html) fornisce un backup del server da disco a disco ad elevate prestazioni che offre una gestione centrale e un repository dei dati. R1Soft CDP protegge i dati a livello di blocco e i blocchi disco univoci sul server vengono memorizzati solo una volta su tutti i punti di ripristino, aumentando l'efficienza dell'archiviazione.
