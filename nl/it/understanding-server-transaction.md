---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Descrizione di una transazione server

Operazioni quali il provisioning di un server su {{site.data.keyword.Bluemix_short}}, il caricamento di un sistema operativo o l'installazione di software vengono messe in una *transazione*.  Una transazione è una serie di passi automatizzata eseguita dai sistemi di gestione {{site.data.keyword.Bluemix_notm}} per configurare i server del cliente.

Se uno dei tuoi server si trova attualmente in una transazione, viene visualizzato un link nelle note sul server negli elenchi hardware. Puoi fare clic su questo link per vedere quali transazioni sono in sospeso per quello specifico server. Ti verrà quindi presentata una tabella che elenca i dati per la transazione corrente in corso.

* **ID** è l'ID interno della transazione. Se inoltri un ticket relativo a una transazione, ricordati di includere questo numero.
* **Group** è una breve descrizione del tipo di transazione. Ad esempio *MS OS Reload* significa che è in corso il ricaricamento del sistema operativo Microsoft sul computer.
* **Current Status** è il nome dell'attuale passo della transazione. Ad esempio *INSTALL_OS* è un passo della transazione per *MS OS Reload*, il che significa che Windows è attualmente in fase di installazione sul computer.
* **Elapsed Time e Average Time** funzionano insieme. Elapsed Time indica da quanto è in esecuzione il passo di transazione corrente. Average Time mostra quanto tempo impiega in media questo passo. Se Elapsed Time è molto più lungo di Average Time, sarebbe opportuno aprire un ticket di supporto per lo stato.
