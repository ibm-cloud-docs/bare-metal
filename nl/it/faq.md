---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-16"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Domande frequenti: server bare metal
{: #bm-faq}

## Cos'è la modalità di avvio UEFI?
{: faq}
L'UEFI (Unified Extensible Firmware Interface) è una specifica per l'interfaccia software tra un sistema operativo e un firmware.

Il supporto IBM Cloud per la modalità di avvio BIOS sta venendo eliminato a favore di UEFI.

Per ulteriori informazioni su UEFI, vedi la tua documentazione sul produttore dell'hardware o vai a [https://uefi.org/](https://uefi.org/)

## Perché il mio BIOS sta chiedendo una password?
{: faq}

Attualmente, {{site.data.keyword.cloud}} non ti fornisce l'accesso diretto al tuo BIOS, per vari motivi. Tuttavia, puoi modificare il BIOS. Se devi modificare qualcosa nel BIOS, compreso l'ordine di avvio, crea un ticket in Supporto > Aggiungi ticket tramite [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/){: new_window} e richiedi le specifiche modifiche di cui hai bisogno.

\*\*NOTA\*\* Questo richiede l'esecuzione di un riavvio del tuo server; ti invitiamo pertanto a essere pronto ad approvare un riavvio e/o fornire un intervallo di tempo in cui vorresti venisse apportata la modifica.

## Fornite dei ricaricamenti del sistema operativo gratuiti?
{: faq}

I ricaricamenti del sistema operativo automatizzati sono gratuiti e possono essere eseguiti tramite [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/){: new_window}. Includono ricaricamenti del sistema operativo personalizzati (modifica dei sistemi operativi, aggiunta/rimozione di pannelli di controllo, modifica delle partizioni e così via).  Per ulteriori informazioni sull'esecuzione di un ricaricamento del sistema operativo, consulta la [procedura di ricaricamento del sistema operativo](/docs/infrastructure/software?topic=software-reloading-the-os).


## L'unità primaria sul mio server bare metal si presenta come /dev/sdb. Cos'è che non va?
{: faq}

La causa potrebbe essere il disco virtuale di IPMI che prende lo slot /dev/sda. Puoi eseguirne senza alcun rischio la disabilitazione stabilendo una connessione a IPMIView e accedendo alla scheda Virtual Media. Seleziona **Options > Disable** e fai clic sul pulsante **Apply** per apportare la modifica. Al successivo riavvio del {{site.data.keyword.baremetal_short}}, l'unità primaria visualizzerà /dev/sda.


## Perché la velocità della CPU è errata?
{: faq}

Poniamo il caso che tu acceda a un server per controllare le informazioni sulla CPU e noti che la velocità dei processori non era corretta. Questa discrepanza può essere dovuta a EIST (Enhanced Intel SpeedStep Technology). EIST è il nome Intel per la tecnologia di ridimensionamento della frequenza dinamico.  Questa tecnologia è detta anche *Limitazione CPU* o *regolazione della risposta del bus* (bus slewing) nei sistemi meno recenti.  Alcuni sistemi AMD hanno delle tecnologie simili chiamate *Cool'N'Quiet* o *PowerNow!*.  Pur non essendo tutte uguali, queste tecnologie hanno lo stesso obiettivo, ossia ridurre il consumo energetico e la produzione di calore quando il processore non è utilizzato in modo intensivo rallentando la velocità della CPU. Quando il server è di nuovo sotto carico, aumentano la velocità di clock come necessario.

Se vuoi sapere se il processore Intel sul tuo server supporta SpeedStep, utilizza questa procedura dal portale clienti:
1. Fai clic su **Dispositivi**.
* Identifica il tuo server nell'elenco.
* Fai clic sul nome server per visualizzare i **Dettagli dispositivo**.
* Individua la sottosezione denominata **Hardware** per trovare il numero di modello della CPU del processore del server.
* Con il numero di modello del processore del server, vai a [Intel Processor Finder ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://processorfinder.intel.com/){: new_window} e usa questo numero per trovare ulteriori informazioni sul processore e per sapere se supporta Enhanced Intel SpeedStep Technology.

EIST è una tecnologia consolidata. È insolito dover disattivare EIST. Tuttavia, se decidi che non vuoi usare questa funzione, apri un ticket con il team di supporto per disabilitare questa funzione.  La disabilitazione di questa funzione prevede il riavvio del server.


## Cosa devo fare se il mio server bare metal ha del firmware obsoleto?
{: faq}

È importante tenere il firmware aggiornato per assicurarti che il tuo server bare metal disponga di una compatibilità e una stabilità ottimali dei dispositivi. Se una versione firmware {{site.data.keyword.baremetal_short}} è obsoleta, il firmware può anche essere aggiornato selezionando il server bare metal dall'elenco dispositivi e selezionando **Update Firmware** dal menu delle azioni.

Puoi avviare un aggiornamento firmware durante il processo di [Ricaricamento SO](/docs/infrastructure/software?topic=software-reloading-the-os) in [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/){: new_window}.

## Cosa succede alle unità nei server bare metal quando un cliente non ne ha più bisogno?
{: faq}

Dopo l'annullamento, un server viene automaticamente spostato su una VLAN di recupero per un tempo di attesa impostato. Una volta completato, vengono avviati i processi di recupero e l'unità viene eliminata utilizzando gli algoritmi DOD 5220.22-M.  Il recupero viene tracciato tramite il numero seriale sull'unità. Dopo il completamento, il server viene spostato nel provisioning per la riassegnazione. Un malfunzionamento dell'unità richiede un intervento manuale e le unità raggiungono il termine del ciclo di vita.

Il processo di termine del ciclo di vita viene avviato quando si presenta un malfunzionamento o se la validità o la dimensione sono al di fuori del supporto. Quando si verifica una di queste condizioni, le unità vengono eliminate come descritto precedentemente. Una volta completato il processo di eliminazione, l'unità viene fisicamente distrutta rompendo, frantumando o facendo a pezzi l'unità.  Il processo di distruzione fisica viene tracciato tramite il numero seriale sull'unità. 

## Posso vedere quali server bare metal sono disponibili per l'acquisto?
{: faq}

Sì! Puoi ora vedere quali server sono disponibili in quali data center quando esegui il provisioning di un server bare metal. Ma questa opzione è disponibile solo per l'offerta oraria. Non puoi vedere la disponibilità server con l'offerta mensile. Per ulteriori informazioni sul provisioning di un server bare metal, vedi [Selezione dai server di provisioning veloce](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## Cos'è incluso con il mio server bare metal riservato?
{: faq}

CPU, RAM, unità disco e RAID sono inclusi nella prenotazione per il termine contrattuale. Se hai bisogno di larghezza di banda più elevata, maggiore capacità di archiviazione, sistema operativo e software di terze parti, i costi di questi componenti aggiuntivi vengono addebitati mensilmente.

## Cosa succede al termine del mio contratto del server bare metal riservato?
{: faq}

Il tuo servizio cloud continua in base a un periodo di funzionamento mensile al costo in vigore alla scadenza del tuo contratto.
