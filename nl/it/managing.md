---


copyright:

  years: 2016, 2018
lastupdated: "2018-04-02"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Gestione dei server bare metal
{: #managing}


Puoi arrestare, avviare, riavviare e annullare i server.
{:shortdesc}

## Replica di un'istanza del server
Puoi copiare o clonare un'istanza del server bare metal per replicare la configurazione del server e avere in breve tempo un nuovo server operativo.
{:shortdesc}

Per clonare l'istanza:
 1. Vai al menu e seleziona **Configura replica**. Vengono copiate tutte le configurazioni. Non vengono copiati dati o contenuto.
 2. Immetti un nome server univoco.
 3. Specifica il nome dominio.

## Ricaricamento del sistema operativo
Di tanto in tanto, sarebbe opportuno ricaricare il sistema operativo sul tuo server.
{:shortdesc}

Per ricaricare il sistema operativo:
 1. Esegui un backup di tutti i dati prima di iniziare. Se questo passo viene tralasciato, tutti i dati esistenti vanno perduti e non è possibile recuperarli.
 2. Vai al menu e seleziona **Ricaricamento del sistema operativo**. Puoi selezionare una delle seguenti opzioni:
  * Passare a un sistema operativo differente e ricominciare con le nuove configurazioni.
  * Conservare il sistema operativo esistente con le configurazioni correnti cancellando però il server per ricominciare.

Durante il ricaricamento del sistema operativo, il server sarà offline e non sarà disponibile per l'uso. Il tempo del ricaricamento varia a seconda della capacità del server e del sistema operativo. Se hai definito uno script di provisioning, tutte le configurazioni verranno ripristinate dopo che il ricaricamento sarà stato completato. Se era stato eseguito un backup dei tuoi dati prima del ricaricamento del sistema operativo, puoi caricarli sul server quando sarà disponibile.

## Eliminazione dell'istanza del server
Puoi eliminare l'istanza del server bare metal in qualsiasi momento se non ti serve più e non vuoi che ti venga addebitata.
{:shortdesc}

Per eliminare l'istanza, vai al menu e seleziona **Annulla server**.

## Spegnimento di un server
Puoi creare un server in anticipo per la preparazione all'uso  Dopo che hai creato il server, spegnilo per assicurarti che niente venga modificato e che nessuno possa accedervi. Quando sei pronto, puoi accendere il server e averlo a tuo disposizione nel giro di pochi minuti.
{:shortdesc}

Per spegnere il server, vai al menu e seleziona **Accendi/Spegni**. Gli addebiti a tuo carico continueranno anche mentre il server è spento.

**Nota:** se il server è spento, rimane in tale stato e devi accenderlo manualmente.
