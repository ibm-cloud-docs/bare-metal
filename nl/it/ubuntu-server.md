---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Installazione del server Ubuntu su un server bare metal

Se vuoi utilizzare un sistema operativo non fornito da {{site.data.keyword.IBM&reg; Cloud}}, puoi eseguirne l'installazione nei server bare metal montando le ISO personalizzate (immagini disco). Per montare una ISO, caricalo sull'archiviazione file (NAS) associata al server. Per caricare una ISO su NAS, usa le seguenti procedure per montare una ISO con IPMI.
1. Ordina il server bare metal con nessun sistema operativo (**No Operating System**) 
* Puoi anche selezionare il sistema operativo gratuito (ad es. CentOS) come sistema operativo che può essere utilizzato per stabilire una connessione alla NAS.
* Ordina l'archiviazione NAS per memorizzare la ISO avviabile. Se già hai qualche server CIFS Windows, puoi utilizzarlo per condividere l'immagine ISO. Con questo server CIFS Windows, otterrai la NAS legacy con una capacità di 20GB. Dopo il provisioning della NAS, puoi vederne la descrizione dal portale clienti.
* Scarica l'immagine ISO da https://www.ubuntu.com/download/server.
* Carica l'immagine ISO sulla NAS o sul server CIFS Windows. Se hai l'archiviazione NAS, puoi caricare il file di immagine ISO utilizzando FTP.

  Procedura FTP di esempio:
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* Stabilisci una connessione VPN a {{site.data.keyword.Bluemix_notm}} con IPMI. Puoi avviare il menu VPN dal menu Supporto o dal seguente URL:[Accesso VPN](http://www.softlayer.com/VPN-Access)
* Monta l'immagine ISO dal menu IPMI Virtual Media utilizzando la connessione a IPMI sull'IP di gestione.
  1. Visualizza le credenziali IPMI
  * Accedi a IPMIView
  * Apri la scheda Virtual Media
  * Ti serve un utente root con privilegi di amministratore su IPMI. Se i privilegi si presentano come *Operatore*, apri un ticket di supporto per modificare i privilegi in Amministratore.
  * Compila i dettagli di connessione dell'immagine ISO
    Share host = L'indirizzo IP della NAS<br/Esempio: 10.3.x.x
    Path to image = Il nome del file ISO, con una formattazione come la seguente: \NomeutenteNAS\nomefileimmagine.iso (ossia \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    User = Il nome utente della NAS
    Password = La password per la NAS
  * Fai clic sul pulsante **Mount**
  * Conferma il dispositivo
* Fai clic e avvia KVM Viewer e apri la pagina Virtual Storage dal menu Virtual Media. Se esegui correttamente il montaggio della tua immagine ISO come dispositivo CDROM, vedrai la descrizione del dispositivo in **Connection Status History**.
* Richiedi che il tuo server esegua l'avvio del suo CD-ROM virtuale come primo dispositivo tramite il ticket SoftLayer. Completa questa richiesta per ogni server. Modifichi l'impostazione di avvio dopo l'installazione del sistema operativo.
  **Nota**: potresti non aver bisogno di contattare il supporto per modificare l'ordine di avvio nel BIOS. Dipende dal tuo server. Prova a riavviare una volta per confermare l'ordine di avvio.
* Riavvia il server dalla vista KVM.
* Installa il sistema operativo dall'immagine ISO montata.
* Installa il sistema operativo Ubuntu sul server bare metal dall'ISO.
* Configura le impostazioni di rete (indirizzo IP/sottorete/gateway/DNS ecc). Se non ne esegui correttamente la configurazione durante il passo di installazione, puoi stabilire una connessione a questo server solo tramite la console KVM dopo il riavvio.

* Smonta il supporto virtuale. Devi smontare il supporto virtuale dal server tramite la scheda IPMI Virtual Media.
* Riavvia il server.
* Dopo il riavvio, puoi accedere al server tramite SSH.
