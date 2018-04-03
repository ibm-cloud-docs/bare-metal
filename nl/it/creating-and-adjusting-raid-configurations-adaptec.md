---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Creazione e regolazione delle configurazioni RAID Adaptec

Il Bios RAID Adaptec ti consente di configurare e gestire la tua impostazione RAID. Usa questo BIOS se stai utilizzando la nostra opzione di [Nessun sistema operativo](introduction-no-os.html) e vuoi impostare una specifica configurazione di unità.

## Accesso al dispositivo IPMI per interagire con il Bios RAID

Indipendentemente dal fatto che la tua macchina abbia un controller Adaptec o un controller LSI, avrai bisogno di accedere al server utilizzando IPMI per interagire con il Bios RAID. Per interagire con IPMI, dovrai prima stabilire una connessione alla VPN {{site.data.keyword.IBM&reg; Cloud}} Adaptec.
1. Accedi alla VPI tramite [SSL](/infrastructure/vpn/ssl-vpn-connections.html) o PPTP. Fai riferimento alla [pagina sull'argomento VPN](/infrastructure/vpn/index.html).
* Accedi all'Elenco dispositivi nel [Portale clienti](https://control.softlayer.com/). Fai riferimento a [Accedi all'elenco dispositivi](/vsi/vsi_managing.html).
* Fai clic sul dispositivo al quale vuoi accedere.
* Seleziona la scheda Remote Mgmt per trovare i dettagli di accesso IPMI del tuo server.
* Inserisci l'IP del tuo dispositivo IPMI nel browser ed esegui l'accesso.
* Per iniziare a interagire con la console remota, fai clic su Remote Control > Console Redirection.

## Creazione di array RAID

Durante il processo di avvio, premi Ctrl+A per accedere al BIOS Raid.

Per iniziare a configurare il tuo RAID, vai a Logical Device Configuration (prima opzione). Questo esegue la scansione della topologia delle tue unità e visualizza un menu in cui puoi gestire gli array, creare gli array e completare altre attività di amministrazione dell'unità.

Il seguente esempio mostra come creare un array. Ti viene presentato un elenco di unità disponibili da utilizzare nella creazione del tuo array RAID.

1. Per selezionare le unità, premi la barra spaziatrice per popolare la casella *Selected Drives*.
* Dopo che hai selezionato tutte le unità che desideri utilizzare nel tuo array, premi INVIO per andare al passo di configurazione del RAID.
* Scegli il tipo di RAID che desideri. Se hai bisogno di assistenza a determinare quale configurazione di RAID risponde meglio alle tue esigenze, consulta le [Domande frequenti da Adaptec](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm).
* Fornisci un'etichetta di array durante la configurazione. È buona prassi includere il tipo di RAID nell'etichetta (ad esempio: RAID10-A).
* Premi Invio per spostarti nelle restanti impostazioni. Usa i valori predefiniti.

Dopo che hai completato la configurazione, seleziona Done; il RAID viene creato. Puoi vedere il nuovo array selezionando 'Manage Arrays' dal menu principale. Per uscire dal programma di utilità di configurazione, premi il tasto ESC finché non ti verrà richiesto di uscire dal BIOS Adaptec.

## Rimozione di array esistenti

Se devi rimuovere un array esistente, vai a Manage Arrays > Seleziona l'array da rimuovere e premi Delete e confermare.

## Configurazioni di esempio

1. Su un server con un totale di 6 unità, puoi configurare 2 SSD in un RAID0 per il tuo sistema operativo e 4 unità aggiuntive in un RAID10 per i tuoi dati effettivi. Questo ti consente di ricaricare rapidamente il sistema operativo del server senza ripristinare i tuoi dati di servizio o sito se ti trovi sull'array secondario.

* Su un server cPanel, hai /var e /home su array RAID SSD separati. Poiché sono le due directory con l'I/O più intensivo su un server cPanel, puoi potenzialmente ridurre il tempo di risposta del sito con le seguenti impostazioni:
  * RAID0 (2 unità SATA) - /
  * RAID0 (2 unità SSD) - /var
  * RAID0 (2 unità SSD) - /home
  * RAID10 (4 unità SATA) - /backup

* Utilizza un singolo array RAID per configurare più partizioni logiche. Ad esempio, utilizza due unità 4TB configurate in un RADI1. Puoi partizionare il RAID perché risponda alle tue esigenze. Ad esempio:
  * Partizione primaria di 100GB per il tuo sistema operativo
  * Seconda partizione di 500GB per i tuoi dati
  * Terza partizione del restante spazio per i backup
