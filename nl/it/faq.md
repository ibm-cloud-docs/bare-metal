---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Domande frequenti: server bare metal

## Perché il mio BIOS sta chiedendo una password?

Attualmente {{site.data.keyword.cloud}}, non ti fornisce l'accesso diretto al tuo BIOS. I motivi sono diversi, ma questo non significa che non puoi apportare modifiche al BIOS. Se devi modificare qualcosa nel BIOS, compreso l'ordine di avvio, crea un ticket in Supporto > Aggiungi ticket tramite il [Portale clienti](control.softlayer.com) e richiedi le specifiche modifiche di cui hai bisogno.

\*\*NOTA\*\* Questo richiederà l'esecuzione di un riavvio del tuo server; ti invitiamo pertanto a essere pronto ad approvare un riavvio e/o fornire un intervallo di tempo in cui vorresti venisse apportata la modifica.

## Fornite dei ricaricamenti del sistema operativo gratuiti?

I ricaricamenti del sistema operativo automatizzati sono gratuiti e possono essere eseguiti tramite il [Portale clienti](control.softlayer.com). Includono ricaricamenti del sistema operativo personalizzati (modifica dei sistemi operativi, aggiunta/rimozione di pannelli di controllo, modifica delle partizioni e così via). Per informazioni dettagliate sull'esecuzione di un ricaricamento del sistema operativo, consulta la [procedura di ricaricamento del sistema operativo](../vsi/vsi_perform_os_reload.html).


## L'unità primaria sul mio server bare metal si presenta come /dev/sdb. Cos'è che non va?

La causa potrebbe essere il disco virtuale di IPMI che prende lo slot /dev/sda. È possibile eseguirne senza alcun rischio la disabilitazione stabilendo una connessione a IPMIView e accedendo alla scheda Virtual Media. Seleziona **Options > Disable** e fai clic sul pulsante **Apply** per apportare la modifica. Al successivo riavvio del {{site.data.keyword.baremetal_short}}, l'unità primaria visualizzerà /dev/sda.


## Perché la velocità della CPU è errata?

Poniamo il caso che tu acceda a un server per controllare le informazioni sulla CPU e noti che la velocità dei processori non era corretta. Questa discrepanza può essere dovuta a EIST (Enhanced Intel SpeedStep Technology). EIST è il nome Intel per la tecnologia di ridimensionamento della frequenza dinamico.  Questa tecnologia è detta anche *Limitazione CPU* o *regolazione della risposta del bus* (bus slewing) nei sistemi meno recenti. Su alcuni sistemi AMD, ci sono delle tecnologie simili chiamate *Cool'N'Quiet* o *PowerNow!*.  Pur non essendo tutte uguali, queste tecnologie hanno lo stesso obiettivo, ossia ridurre il consumo energetico e la produzione di calore quando il processore non è utilizzato in modo intensivo rallentando la velocità della CPU. Quando il server è di nuovo sotto carico, aumentano la velocità di clock come necessario.

Se vuoi sapere se il processore Intel sul tuo server supporta SpeedStep, nel portale clienti: 
1. Fai clic su **Dispositivi**.
* Identifica il tuo server nell'elenco.
* Fai clic sul nome server per visualizzare i **Dettagli dispositivo**.
* Individua la sottosezione denominata **Hardware** per trovare il numero di modello della CPU del processore del server.
* Con il numero di modello del processore del server, vai a [Intel Processor Finder](http://processorfinder.intel.com/) e usa questo numero per trovare ulteriori informazioni sul processore e per sapere se supporta Enhanced Intel SpeedStep Technology.

EIST è una tecnologia consolidata. Non dovresti avere alcun motivo per disattivare EIST. Tuttavia, se decidi che non vuoi usare questa funzione, apri un ticket con il team di supporto per disabilitare questa funzione. La disabilitazione di questa funzione prevede il riavvio del server.


## Cosa devo fare se il mio server bare metal ha del firmware obsoleto?

Analogamente agli aggiornamenti software, è importante tenere il firmware aggiornato per garantire una compatibilità e una stabilità ottimali dei dispositivi. Se il firmware di un {{site.data.keyword.baremetal_short}} è obsoleto, un suo aggiornamento può essere avviato durante un processo di ricaricamento del sistema operativo ([OS Reload](../infrastructure/software/vsi_reload_os.html)) nel [Portale clienti](https://control.softlayer.com).

Puoi anche aggiornare il firmware selezionando il server bare metal dall'elenco dispositivi e selezionando **Update Firmware** dal menu a discesa delle azioni.
