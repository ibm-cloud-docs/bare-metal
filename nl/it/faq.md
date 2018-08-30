---

copyright:
  years: 2014, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Domande frequenti: server bare metal

## Perché il mio BIOS sta chiedendo una password?

Attualmente {{site.data.keyword.cloud}}, non ti fornisce l'accesso diretto al tuo BIOS per diversi motivi. Puoi tuttavia modificare il BIOS. Se devi modificare qualcosa nel BIOS, compreso l'ordine di avvio, crea un ticket in Supporto > Aggiungi ticket tramite il [Portale clienti](https://control.softlayer.com/) e richiedi le specifiche modifiche di cui hai bisogno.

\*\*NOTA\*\* Questo richiede l'esecuzione di un riavvio del tuo server; sii pertanto pronto ad approvare un riavvio e/o fornire un intervallo di tempo in cui vorresti venisse apportata la modifica.

## Fornite dei ricaricamenti del sistema operativo gratuiti?

I ricaricamenti del sistema operativo automatizzati sono gratuiti e possono essere eseguiti tramite il [Portale clienti](https://control.softlayer.com/). Includono ricaricamenti del sistema operativo personalizzati (modifica dei sistemi operativi, aggiunta/rimozione di pannelli di controllo, modifica delle partizioni e così via).  Per ulteriori informazioni sull'esecuzione di un ricaricamento del sistema operativo, consulta la [procedura di ricaricamento del sistema operativo](../vsi/vsi_perform_os_reload.html).


## L'unità primaria sul mio server bare metal si presenta come /dev/sdb. Cos'è che non va?

La causa potrebbe essere il disco virtuale di IPMI che prende lo slot /dev/sda. Puoi eseguirne senza alcun rischio la disabilitazione stabilendo una connessione a IPMIView e accedendo alla scheda Virtual Media. Seleziona **Options > Disable** e fai clic sul pulsante **Apply** per apportare la modifica. Al successivo riavvio del {{site.data.keyword.baremetal_short}}, l'unità primaria visualizzerà /dev/sda.


## Perché la velocità della CPU è errata?

Poniamo il caso che tu acceda a un server per controllare le informazioni sulla CPU e noti che la velocità dei processori non era corretta. Questa discrepanza può essere dovuta a EIST (Enhanced Intel SpeedStep Technology). EIST è il nome Intel per la tecnologia di ridimensionamento della frequenza dinamico.  Questa tecnologia è detta anche *Limitazione CPU* o *regolazione della risposta del bus* (bus slewing) nei sistemi meno recenti.  Alcuni sistemi AMD hanno delle tecnologie simili denominate *Cool'N'Quiet* o *PowerNow!*.  Pur non essendo tutte uguali, queste tecnologie hanno lo stesso obiettivo, ossia ridurre il consumo energetico e la produzione di calore quando il processore non è utilizzato in modo intensivo rallentando la velocità della CPU. Quando il server è di nuovo sotto carico, aumentano la velocità di clock come necessario.

Se vuoi sapere se il processore Intel sul tuo server supporta SpeedStep, usa questa procedura dal portale clienti:
1. Fai clic su **Dispositivi**.
* Identifica il tuo server nell'elenco.
* Fai clic sul nome server per visualizzare i **Dettagli dispositivo**.
* Individua la sottosezione denominata **Hardware** per trovare il numero di modello della CPU del processore del server.
* Con il numero di modello del processore del server, vai a [Intel Processor Finder](http://processorfinder.intel.com/) e usa questo numero per trovare ulteriori informazioni sul processore e per sapere se supporta Enhanced Intel SpeedStep Technology.

EIST è una tecnologia consolidata. Non è una cosa comune che tu debba disattivare EIST. Tuttavia, se decidi che non vuoi usare questa funzione, apri un ticket con il team di supporto per disabilitare questa funzione.  Per disabilitare questa funzione, il server viene riavviato.


## Cosa devo fare se il mio server bare metal ha del firmware obsoleto?

Analogamente agli aggiornamenti software, è importante tenere il firmware aggiornato per garantire una compatibilità e una stabilità ottimali dei dispositivi. Se il firmware di un {{site.data.keyword.baremetal_short}} è obsoleto, un suo aggiornamento può essere avviato durante un processo di ricaricamento del sistema operativo ([OS Reload](../infrastructure/software/vsi_reload_os.html)) nel [Portale clienti](https://control.softlayer.com).

Puoi anche aggiornare il firmware selezionando il server bare metal dall'elenco dispositivi e selezionando **Update Firmware** dal menu delle azioni.

## Cosa succede alle unità nei server bare metal quando un cliente ha finito con loro?

In caso di annullamento, un server viene automaticamente spostato in una VLAN di recupero per un tempo di permanenza impostato. Una volta completato, i processi di recupero vengono avviati e i dati dell'unità vengono cancellati utilizzando gli algoritmi DOD 5220.22-M. Si tiene traccia del recupero utilizzando il numero di serie sull'unità. Una volta completata l'operazione, il server viene spostato nel provisioning per la riassegnazione. Un malfunzionamento dell'unità richiede un intervento manuale e le unità vengono quindi impostate su una terminazione del ciclo di vita.

Il processo di terminazione del ciclo di vita viene avviato quando si verifica un malfunzionamento o se l'età o la dimensione vanno oltre il supporto. Quando si verifica una qualsiasi di queste condizioni, i dati delle unità vengono cancellati come descritto in precedenza. Una volta completato il processo di cancellazione dei dati, l'unità viene distrutta fisicamente rompendola, frantumandola o triturandola. Si tiene traccia del processo di distruzione fisica utilizzando il numero di serie sull'unità.
