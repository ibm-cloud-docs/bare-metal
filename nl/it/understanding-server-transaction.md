---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

keywords: server transation, {{site.data.keyword.cloud_notm}}, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Descrizione di una transazione server
{: #bm-server-transaction}

Operazioni quali il provisioning di un server su {{site.data.keyword.cloud}}, il caricamento di un sistema operativo o l'installazione di software vengono inserite in una *transazione*.  Una transazione è una serie automatizzata di passi che vengono eseguiti dai sistemi di gestione {{site.data.keyword.cloud_notm}} per configurare i server del cliente.

Se uno dei tuoi server è in una transazione, viene visualizzato un link nelle note del server negli elenchi hardware.  Puoi fare clic su questo link per vedere quali transazioni sono in sospeso per quello specifico server.  Ti viene quindi presentata una tabella che elenca i dati per la transazione corrente in corso.

* **ID** è l'ID interno della transazione.  Se inoltri un ticket relativo a una transazione, ricordati di includere questo numero.
* **Group** è una breve descrizione del tipo di transazione.  Ad esempio *MS OS Reload* significa che è in corso il ricaricamento del sistema operativo Microsoft sul computer.
* **Current Status** è il nome dell'attuale passo della transazione.  Ad esempio *INSTALL_OS* è un passo della transazione per *MS OS Reload*, il che significa che Windows è attualmente in fase di installazione sul computer.
* **Elapsed Time e Average Time** funzionano insieme.  Elapsed Time indica da quanto è in esecuzione il passo di transazione corrente.  Average Time mostra quanto tempo impiega in media questo passo.  Se il tempo trascorso è significativamente più lungo del tempo medio, potresti voler aprire un ticket di supporto per lo stato.
