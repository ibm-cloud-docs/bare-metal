---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

keywords: set up bare metal server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configurazione di un Bare Metal Server
{: #bm-set-up}

Puoi configurare un Bare Metal Server come server dedicato.
{:shortdesc}

## Prima di iniziare
* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Assicurati di disporre di tutte le autorizzazioni di account necessarie e dell'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione di **Gestione utenti** dell'infrastruttura classica può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione dell'accesso al dispositivo](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Configurazione di un Bare Metal Server

Utilizza la seguente procedura per configurare un Bare Metal Server:

1. Dal menu, fai clic su **Dispositivi** > **Elenco dispositivi** e trova il tuo sistema. Tutti i tuoi dispositivi sono dettagliati nell'Elenco dispositivi, dove puoi gestirli ed eseguirne l'upgrade o generare grafici di utilizzo della larghezza di banda.

2. Scegli di gestire il tuo server in uno dei seguenti modi:
  * Fai clic sulla freccia accanto al nome dispositivo per visualizzare un riepilogo e gestire i tuoi dispositivi dalla vista Istantanea.
  * Fai clic sul nome dispositivo del server per visualizzare un elenco dettagliato e gestire i tuoi dispositivi dalla schermata Dettagli del dispositivo.

3. Registra l'indirizzo IP e le credenziali per il server in un luogo sicuro in modo da poter accedere rapidamente ai dettagli senza dover accedere al portale clienti ogni volta che ne hai bisogno. Puoi registrare questi dettagli sia per un singolo dispositivo che per tutti i dispositivi associati al tuo account:
  * Visualizza gli IP dei singoli dispositivi dall'Elenco dispositivi.
  * Visualizza le password root dei singoli dispositivi nella vista Istantanea per il dispositivo.
  * Visualizza più IP dispositivo utilizzando l'opzione **Scarica CSV** dall'**Elenco dispositivi**. Quindi, seleziona **Scarica CSV** dall'ingranaggio delle **Impostazioni** per scaricare un elenco completo di dispositivi e di dettagli nel formato foglio di calcolo.

4. Aggiorna le credenziali per i sistemi operativi e altri software. A tutti i software caricati sul dispositivo durante il processo di provisioning sono state assegnate credenziali temporanee. Puoi visualizzare e gestire queste credenziali nella scheda Password di ciascun dispositivo nel portale clienti. Utilizza queste credenziali temporanee per accedere al tuo software per la prima volta. Quindi, modifica la password del tuo software seguendo le pratiche di password complesse. Crea una password che comprenda una combinazione di lettere, numeri e simboli. Facoltativamente, puoi memorizzare gli aggiornamenti delle password nella scheda Password per ciascun dispositivo. Tuttavia, quando memorizzi le password nel portale clienti, qualsiasi persona con accesso all'account e autorizzazioni appropriate può visualizzare le password memorizzate nella schermata Password.

5. Accedi al tuo server sulla rete privata. Puoi utilizzare la rete privata dell'infrastruttura {{site.data.keyword.cloud_notm}} per interagire con i tuoi dispositivi tramite desktop remoto (RDP) utilizzando SSH e KVM su IP. Puoi utilizzare lo strumento Accesso VPN per la connessione della rete privata all'endpoint VPN SSL più vicino o all'endpoint di tua scelta. L'accesso VPN è necessario anche per interagire con diversi servizi. Per accedere alla rete privata, modifica l'accesso VPN dell'utente dall'Elenco utenti. Per accedere all'Elenco utenti, fai clic su **Account** > **Utenti** > **Elenco utenti**. Utilizza la pagina [Virtual Private Network ![Icona link esterno](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} per la connessione a una delle varie opzioni VPN.

6. Configura il monitoraggio per controllare lo stato del tuo server e sapere quando ridimensionare. Puoi utilizzare il monitoraggio standard o i servizi di monitoraggio Nimsoft. Puoi utilizzare il monitoraggio standard, o di base, nel metodo ping-and-respond (effettua ping e rispondi) utilizzando un ping lento o di servizio dal portale clienti. Puoi anche utilizzare il monitoraggio Nimsoft, o avanzato, dal portale clienti o in 1 dei 3 livelli: base, avanzato e premium.

7. Proteggi il tuo sistema. Utilizza i firewall hardware disponibili per proteggere il tuo dispositivo. Puoi eseguire il provisioning di firewall hardware su richiesta senza tempi di inattività, se vengono stabilite correttamente delle regole, per proteggere il tuo server da attività indesiderate. Dopo aver ordinato il firewall, è necessario abilitarlo e impostare le regole.

8. Pianifica i backup per garantire che i tuoi dati siano memorizzati in modo sicuro al di fuori del tuo dispositivo e riuscire a ricaricarli se vengono persi. Puoi scegliere tra vari servizi di backup per memorizzare i tuoi dati in un luogo sicuro:
  * IBM Cloud Backup è un sistema di backup automatizzato basato sull'agent. IBM Cloud Backup è una soluzione “set-and-forget” (imposta e dimentica) per la gestione del tuo dispositivo. È compatibile con i software Microsoft tra cui Exchange e SQL attraverso plugin aggiuntivi. Gli utenti di IBM Cloud Backup interagiscono con questo servizio tramite l'applicazione basata sul web WebCC di IBM Cloud Backup.
  * R1Soft CDP (Continuous Data Protection) può essere installato sul tuo server o sulla macchina virtuale autogestita. È consigliabile se desideri una singola interfaccia per gestire tutti i tuoi backup. Interagisci con R1Soft CDP tramite il tuo sistema di gestione proprietario, che consente di installare gli agent su macchine virtuali e offre plugin di database per ulteriori funzionalità.
