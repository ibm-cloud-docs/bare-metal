---

copyright:

  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configurazione di un Bare Metal Server
{: #customerportal_setupbaremetal}

Puoi configurare un Bare Metal Server come un server dedicato.
{:shortdesc}

Attieniti alla seguente procedura per configurare un Bare Metal Server:

1. Esegui l'accesso al portale clienti {{site.data.keyword.BluSoftlayer_full}} con le tue credenziali univoche.

2. Dal menu, fai clic su **Devices** > **Device list** e trova il tuo sistema. Tutti i tuoi dispositivi sono dettagliati nell'elenco dispositivi, dove puoi gestire, ed eseguire upgrade di, dispositivi o generare grafici di utilizzo della larghezza di banda.

3. Scegli di gestire il tuo server in uno dei seguenti modi:
  * Fai clic sulla freccia accanto al nome dispositivo per visualizzare un riepilogo e gestire i dispositivi dalla vista Snapshot.
  * Fai clic sul nome dispositivo del server per visualizzare un elenco dettagliato e gestire i tuoi dispositivi dalla schermata Device Details.

4. Registra l'indirizzo IP e le credenziali per il server in un luogo sicuro in modo da poter accedere rapidamente ai dettagli senza dover accedere al portale clienti ogni volta che ne hai bisogno. Puoi registrare questi dettagli sia per un singolo dispositivo che per tutti i dispositivi associati al tuo account:
  * Visualizza gli IP dei singoli dispositivi dall'elenco dispositivi (Device List).
  * Visualizza le password root dei singoli dispositivi nella vista Snapshot per il dispositivo.
  * Visualizza più IP dispositivo utilizzando l'opzione **Download CSV** dal **Device List**. Seleziona quindi **Download CSV** dall'ingranaggio **Settings** per scaricare un elenco completo di dispositivi e di dettagli nel formato foglio di calcolo.

5. Aggiorna le credenziali per i sistemi operativi e altri software. A tutti i software caricati sul dispositivo durante il processo di provisioning erano state assegnate credenziali temporanee. Puoi visualizzare e gestire queste credenziali nella scheda Passwords di ciascun dispositivo nel portale clienti. Utilizza queste credenziali temporanee per accedere al tuo software per la prima volta, quindi modifica la password per il tuo software utilizzando una password complessa che comprenda una combinazione di lettere, numeri e simboli. Facoltativamente, puoi memorizzare gli aggiornamenti delle password nella scheda Passwords per ciascun dispositivo; tuttavia, quando memorizzi le password nel portale clienti, qualsiasi persona con accesso all'account e autorizzazioni appropriate può visualizzare le password memorizzate nella schermata Passwords.

6. Accedi al tuo server sulla rete privata. Puoi utilizzare la rete privata dell'infrastruttura {{site.data.keyword.BluSoftlayer_notm}} per interagire con i tuoi dispositivi tramite desktop remoto (RDP) utilizzando SSH e KVM su IP. Puoi utilizzare lo strumento Accesso VPN per la connessione della rete privata all'endpoint VPN SSL più vicino o all'endpoint di tua scelta. L'accesso VPN è necessario anche per interagire con diversi servizi. Per accedere alla rete privata, modifica l'accesso VPN dell'utente dall'elenco clienti (User List). Per accedere all'elenco clienti, fai clic su **Account** > **Users** > **User list**. Utilizza la pagina [Virtual Private Network ![Icona link esterno](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} per stabilire una connessione a una delle varie opzioni VPN.

7. Configura il monitoraggio per controllare lo stato del tuo server e sapere quando ridimensionare. Puoi utilizzare il monitoraggio standard o i servizi di monitoraggio Nimsoft. Puoi utilizzare il monitoraggio standard, o di base, nel metodo ping-and-respond (effettua ping e rispondi) utilizzando un ping lento o di servizio dal portale clienti. Puoi anche utilizzare il monitoraggio Nimsoft, o avanzato, dal portale clienti o in uno dei tre livelli: base, avanzato e premium.

8. Proteggi il tuo sistema. Utilizza i firewall hardware disponibili per assicurarti che il tuo dispositivo sia sempre protetto. Puoi eseguire il provisioning di firewall hardware su richiesta senza tempi di inattività, se vengono stabilite correttamente delle regole, per proteggere il tuo server da attività indesiderate. Dopo aver ordinato il firewall, è necessario abilitarlo e impostare le regole.

9. Pianifica i backup per garantire che i tuoi dati siano memorizzati in modo sicuro al di fuori del tuo dispositivo e riuscire a ricaricarli se vengono persi. Puoi scegliere da una varietà di servizi di backup per memorizzare i tuoi dati in un'ubicazione sicura:
  * EVault Backup è un sistema di backup automatizzato basato sull'agent. Questa è una popolare soluzione “set-and-forget” (imposta e dimentica) per la gestione del tuo dispositivo. È compatibile con il software Microsoft tra cui Exchange e SQL tramite plug-in aggiuntivi. Gli utenti EVault interagiscono con questo servizio tramite l'applicazione basata sul web WebCC di EVault.
  * R1Soft CDP (Continuous Data Protection) può essere installato sul tuo server o sulla macchina virtuale autogestita. È consigliabile se desideri una singola interfaccia per gestire tutti i tuoi backup. Interagisci con R1Soft CDP tramite il tuo sistema di gestione proprietario, che consente di installare gli agent su macchine virtuali e offre plug-in di database per funzionalità aggiuntive.
