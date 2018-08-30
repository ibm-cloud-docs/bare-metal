---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Montaggio di una ISO su un server bare metal

## Panoramica

Anche se la maggior parte dei clienti {{site.data.keyword.Bluemix_notm}} utilizza uno dei sistemi operativi standard forniti con i nostri server, puoi montare delle ISO (immagini disco) personalizzate sui server. Ci sono tre opzioni per montare le ISO personalizzate.

Perché i metodi funzionino, dovrai essere connesso alla rete privata tramite il servizio SL VPN ,come ad es. [SoftLayer SSL VPN Portal - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login) o tramite un altro server che già hai connesso alla rete.

**Nota:** le immagini del disco hardware Lenovo di dimensioni superiori a 50 MB devono essere montate utilizzando la scheda dell'interfaccia della console IMM > media.

## Opzione 1 (preferita): utilizzo di IPMI (ISO su una condivisione CIFS)

Se già hai l'infrastruttura distribuita su {{site.data.keyword.Bluemix_notm}}, puoi configurare un server esistente per offrire una condivisione CIFS alla rete interna. Puoi quindi montare su un server bare metal qualsiasi ISO presente.

Questo è il metodo preferito per installare un sistema operativo personalizzato su un server bare metal perché esegue l'installazione sulla rete locale, che è molto veloce e può tenere una ISO montata anche se ti disconnetti o vieni disconnesso dall'interfaccia di gestione.

Attieniti alla seguente procedura per installare un sistema operativo personalizzato da una condivisione CIFS:

1. Assicurati di aver messo la ISO nella condivisione CIFS.
* Accedi alla console di gestione IPMI puntando il tuo browser web all'IP specificato in control.https://control.softlayer.com/ e in devices -> il tuo server (device details) -> Remote Mgmt. Vengono qui specificati anche il nome utente e la password.
* Punta il mouse su **Virtual Media** e fai clic su **CD-ROM image**
* Compila i dettagli appropriati e fai clic su **Save and Mount**.
* Non tutti gli utenti dispongono dell'autorizzazione a modificare il BIOS del server. Se necessario, puoi aprire un ticket al supporto richiedendo:
  * I privilegi di amministratore di un utente root su IPMI (per poter modificare la modalità Virtual Media Attach)
  * Modificare la sequenza di avvio in ‘IPMI Virtual Disk’ come prima opzione di avvio.
* Dopo aver apportato queste modifiche, torna alla console di gestione IPMI e vai a configuration -> Remote session e modifica la modalità di collegamento (attach) in: **attach**. In alcune console IPMI meno recenti, puoi tralasciare questa opzione.
* Riavvia il server ed esegui l'avvio dal supporto virtuale.


## Opzione 2: utilizzo di IPMIView (ISO su una condivisione CIFS)

Prerequisiti<br/>
* Disponi di una ISO avviabile
* Un server CIFS Windows o un'archiviazione NAS per memorizzare l'ISO avviabile
* L'ISO è caricata sul File Storage (NAS) associato al server.
* IPMIView è installato o c'è un accesso alla console KVM <!--  * http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* http://knowledgelayer.softlayer.com/procedure/access-kvm-console -->
* Il file ISO è scaricabile utilizzando wget
* Disponi dell'accesso SSH con i privilegi per accedere ai pacchetti e installarli e per creare un montaggio


### Linux e Windows
Attieniti alla seguente procedura per montare una ISO con IPMIView.
1. Tramite un ticket di supporto, richiedi che il tuo server esegua l'avvio dal suo CD-ROM virtuale come primo dispositivo. Ogni dispositivo deve eseguire l'avvio dal suo CD-ROM virtuale associato. Puoi annullare la modifica apportata a questa impostazione dopo che hai installato il sistema operativo.
* Stabilisci una connessione VPN a [VPN](http://www.softlayer.com/VPN-Access). Se stai utilizzando Microsoft Internet Explorer, assicurati di includere .softlayer.com nel tuo elenco Siti attendibili e tieni aggiornato il tuo JAVA.
* Copia il supporto ISO su NAS o sul server CIFS Windows.
  * Stabilisci una connessione al tuo jumpbox Linux utilizzando SSH.
  * Monta la condivisione NAS sul tuo jumpbox Linux:

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * Chiave di parametro del comando mount:
        NAS_SERVER_NAME_ORIP = il nome o l'IP dell'archiviazione NAS.
        /SLN#####-2 = il nome utente e il nome cartella per stabilire una connessione alla tua archiviazione NAS.
        NAS_STORAGE_PW = la password alla tua archiviazione NAS.
        /mnt/nasmount = la cartella per montare l'archiviazione NAS.
  * Modifica la directory alla tua nuova cartella di montaggio NAS.
        cd /mnt/nasmount
  * Scarica il file iso utilizzando wget.
        wget http://www.linktoyouriso.com/isofilename.iso
  Vedrai una conferma della corretta esecuzione del download.
* Scarica IPMIView qui:
      http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* Stabilisci una connessione al server sull'IP di gestione.
      http://knowledgelayer.softlayer.com/procedure/log-ipmiview
      http://knowledgelayer.softlayer.com/procedure/view-ipmi-credentials
* Apri la scheda Virtual Media
* Completa i dettagli della connessione dell'immagine CD-ROM.
  *
    * Share host = l'indirizzo IP dell'archiviazione NAS. Puoi trovare questo valore eseguendo un ping del tuo nome server di archiviazione NAS. Ad esempio, _ping nas501.service.softlayer.com_
    * Share Name = il nome utente dell'archiviazione NAS
    * Path to image = il nome del file ISO, nel seguente formato:
          \nomeutenteNAS\nomeiso.iso (ossia \SLN123456\centos6.iso)
    * User = il nome utente dell'archiviazione NAS
    * Password = la password per l'archiviazione NAS
* Riavvia il server
* Apri la vista KVM Console
* Attieniti ai prompt di sistema per avviare la ISO avviabile (BOOTABLE ISO)
* Installa il sistema operativo
* Somta il supporto virtuale
* Riavvia il server

## Opzione 3: montaggio di una ISO dal tuo computer locale
<a name="option3"></a>

Puoi montare una ISO dal tuo computer locale utilizzando Java iKVM Viewer (console). Ciò ti consentirà di montare una ISO mentre sei connesso alla console. La velocità alla quale avanza l'installazione può variare a seconda della velocità di caricamento e della latenza della tua connessione a Internet e delle prestazioni di java e del tuo computer.

Se non disponi dell'autorizzazione a modificare la BIOS su un server, apri un ticket al supporto richiedendo le seguenti modifiche:
* I privilegi di amministratore di un utente Root su IPMI (per poter modificare la modalità Virtual Media Attach)
* Modificare la sequenza di avvio in ‘IPMI Virtual Disk’ come prima opzione di avvio. (Poiché ISO non è ancora montata, il supporto deve modificare solo la priorità del dispositivo di avvio, per ora).


1. Accedi alla console di gestione IPMI puntando il tuo browser web all'IP specificato in https://control.softlayer.com/.
* Fai clic su Devices > il tuo server (device details) > Remote Mgmt. Specifca il nome utente e la password.
* Fai clic su Configuration > Remote session e modifica la modalità di collegamento (attach) in **attach**. In alcune console IPMI meno recenti, questa opzione non è disponibile e puoi pertanto tralasciare questo passo.
* Fai clic su System > System information per ritornare alla pagina System Information. Vedrai un'icona di fintra della console.
* Fai clic sull'icona della console per aprire la console. Accetta tutte le avvertenze di sicurezza.
* Quando la console è connessa, vedrai il prompt di accesso.
* Fai clic su Virtual Media > Virtual Storage
* Vai alla scheda **CDROM&ISO** e seleziona il file ISO (ISO File) in **Logical Drive Type**
* Fai clic su **Open Image** e seleziona l'ISO sul tuo computer locale
* Fai clic su **Plug in** per inserire l'ISO nell'unità CD-ROM virtuale.
* Fai clic su **OK**.
* Riavvia il server e utilizza l'opzione **boot from the virtual cd-rom drive**. Potresti aver bisogno di utilizzare la tastiera virtuale in iKVM Viewer per selezionare un dispositivo di avvio.

## Risoluzione dei problemi

* Non tutti gli utenti hanno l'accesso predefinito per montare il supporto virtuale. Se si verifica un errore di autorizzazione, contatta il supporto per un aggiornamento alle autorizzazioni utente IPMI root.
* Se una ISO è già montata, verrà visualizzato un messaggio di errore con il testo **There is a disk mounted**. Devi smontare il disco esistente oppure sostituirlo con la nuova ISO. Due ISO non possono essere montate contemporaneamente.
* Poresti dover contattare il supporto per modificare l'ordine di avvio nel BIOS.
* Quando monti una ISO, utilizza VPN SSL (http://vpn.softlayer.com) invece di VPN PPTP.  Una volta stabilita una connessione alla rete VPN, puoi anche accedere all'IPMI di sistema tramite l'indirizzo IPMI (https://<private-ip-IPMI-management>).
* Quando immetti un percorso a una ISO, usa la sintassi di denominazione UNC (Universal Naming Convention) per il percorso, ad esempio:
  _\\<NAS username>\<isoname>.iso_
