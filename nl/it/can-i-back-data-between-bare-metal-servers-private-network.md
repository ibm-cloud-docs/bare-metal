---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Backup e ripristino
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}} fornisce diverse [soluzioni di backup e archiviazione ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud/storage){: new_window} scalabili per soddisfare i tuoi requisiti di backup. Tuttavia, {{site.data.keyword.Bluemix_notm}} non completa i backup dei dispositivi dei clienti. Un utente sul tuo account deve avviare tutti i backup pianificati e una tantum sui tuoi dispositivi.

Se su un account esistono due o più {{site.data.keyword.baremetal_short}}, è possibile eseguire il backup da un dispositivo a un altro. Non viene applicato alcun limite di larghezza di banda per il traffico di rete privata e, pertanto, è possibile eseguire il trasferimento o il backup dei dati tra qualsiasi dispositivo che condivide un account in qualsiasi momento. Diverse soluzioni di backup sono disponibili per {{site.data.keyword.baremetal_short}}, incluse le seguenti soluzioni:

* [IBM Cloud Backup](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started) è una soluzione di backup aziendale che può automatizzare i backup su più server. I dati vengono memorizzati in una SAN (storage area network) aziendale.
* [NAS (Network Attached Storage)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted) è uno standard del settore e fornisce memorizzazione esterna al server per i dati critici. I dati vengono memorizzati in una SAN (storage area network) aziendale.
* [CDR R1Soft](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft) fornisce un backup del server da disco a disco ad elevate prestazioni che offre una gestione centrale e un repository dei dati. R1Soft CDP protegge i dati a livello di blocco e i blocchi disco univoci sul server vengono memorizzati solo una volta su tutti i punti di ripristino, aumentando l'efficienza dell'archiviazione.
