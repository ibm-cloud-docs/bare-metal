---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Creazione di un server bare metal personalizzato
{: #ordering-baremetal-server}

Attieniti alla seguente procedura per creare un {{site.data.keyword.baremetal_short}} personalizzato.

1. Apri il catalogo [{{site.data.keyword.cloud_notm}}](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Seleziona Bare Metal Server.
3. Fai clic su Crea.
4. Sotto l'elenco di server, cerca l'istruzione: **Sei interessato ad altre opzioni di configurazioni? Fai clic qui**. Seleziona questa opzione. Viene visualizzato il modulo server personalizzato.
1. Seleziona un'ubicazione del data center per il tuo server.
* Seleziona un server dalle tre categorie di server facendo clic sul link **Starting Price Per**.
  * SAP Certified Servers (per ulteriori informazioni sul provisioning di un server con certificazione SAP, vedi [{{site.data.keyword.cloud_notm}} SAP-Certified Infrastructure](/docs/bare-metal/bare-metal-sap-applications.html))
  * Single Processor Multi-Core Servers
  * Dual Processor Multi-Core Servers

* Seleziona dalle tue opzioni di configurazione. I campi relativi a **data center**, **RAM** e **sistema operativo** sono obbligatori. Tutti gli altri campi sono facoltativi. Per ulteriori informazioni sui campi facoltativi, vedi **[Opzioni aggiuntive di configurazione del server](#addl-server-options)** .

    **Nota**: viene visualizzato un messaggio di errore se si verifica un conflitto tra il server e il sistema operativo. Un esempio è la selezione di Linux su un server Microsoft SQL.
* Fai clic su **Add to Order**. Viene visualizzata la pagina Checkout.

  Dalla pagina Checkout, puoi tornare alla pagina di configurazione facendo clic su una delle opzioni di riconfigurazione.
* Nella sezione Advanced System Configuration, specifica le opzioni aggiuntive di configurazione. Per ulteriori informazioni, vedi **[Configurazione di sistema avanzata](#adv-system-config)**.

*   Fai clic sulle caselle di spunta **Termini del servizio cloud** e **Accordo servizi di terze parti**.
*   Conferma o immetti le tue informazioni di pagamento e fai clic su **Submit Order**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

  Puoi anche salvare questo ordine senza acquistare facendo clic su **Save as Quote**.

 Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning. L'email di completamento del provisioning include un link alla tua pagina *Device Details* dopo che hai eseguito l'accesso a {{site.data.keyword.cloud_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

 ## Opzioni aggiuntive di configurazione del server
 {: #addl-server-options}

 Hai a disposizione delle opzioni aggiuntive quando esegui il provisioning del tuo server bare metal come ad esempio, tra le altre, quelle relative alla larghezza di banda pubblica, alle velocità delle porte di uplink e agli indirizzi IP secondari pubblici. La tabella 1 descrive le opzioni aggiuntive.


 | **Campo** | **Descrizione** |
 |-------------------|---------------|
 |Sicurezza server|Come ad esempio Trusted Execution Technology (Intel TXT)|
 |Software Guard Extensions|Una sicurezza aumentata per il codice e i dati sensibili (Intel SGX). <br><br>Vedi [Provisioning di un server bare metal con Intel SGX](../bare-metal/bare-metal-provision-SGX.html).|
 |RAM|Scegli un livello di RAM che soddisfi le esigenze del tuo server.|
 |Sistema operativo |Seleziona da CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu oppure Other. |
 |Dischi rigidi |Utilizza lo strumento nell'interfaccia utente per configurare i tuoi dischi rigidi ricompilando i campi in base alla tua selezione del sistema operativo. <br><br> Puoi anche scegliere di utilizzare un'unità SSD Intel Optane. Fai riferimento a [Provisioning di una SSD Intel Optane DC P4800X](../bare-metal/bm-provision_ssd.html).
 |Larghezza di banda pubblica |Determina la quantità di dati che può essere trasferita tramite l'interfaccia pubblica durante un mese. Per gli ambienti di test, che richiedono che i dati di installazione vengano trasferiti tramite questa interfaccia, i valori devono essere adattati oltre la quantità di dati trasferita inizialmente. Prendi in considerazione la [Content Delivery Network {{site.data.keyword.cloud_notm}}](https://www.ibm.com/cloud/cdn) per inviare un carico di dati iniziale a uno dei data center {{site.data.keyword.cloud_notm}}. È possibile eseguire un upgrade di tutti i {{site.data.keyword.baremetal_short}} per includere una larghezza di banda illimitata. Tutti i dispositivi illimitati sono su porte private e dedicate.|
 |Velocità porta di uplink |Determina la velocità delle interfacce interne ed esterne. |
 |Indirizzi IP secondari pubblici |Assegna più indirizzi IP al tuo server. A seconda del tuo scenario, potresti aver bisogno di ulteriori indirizzi IP assegnati al tuo server. Ulteriori indirizzi IPv4 sono disponibili in quantità di 1, 2, 4, 8, 16 o 32. |
 |Indirizzi IPv6 primari |Assegnati alle interfacce interne e a quelle esterne del tuo server. |
 |Indirizzi IPv6 statici pubblici |Assegna più indirizzi IPv6 da un blocco /64. |
 |Componenti aggiuntivi del sistema operativo|Seleziona opzioni quali VMware, soluzioni di backup, pannello di controllo, database, Firewall hardware e software, Protezione antivirus e spyware e Rilevamento e prevenzione delle intrusioni. <br><br>Ti consigliamo vivamente di allineare il tuo dipartimento di sicurezza aziendale con il supporto {{site.data.keyword.cloud_notm}} per discutere i dettagli di queste opzioni.
 |Evault |Uno strumento di backup basato sugli agent che può essere installato sul tuo server per replicare i backup tra i server. |
 |Componenti aggiuntivi del servizio|Seleziona eventuali componenti aggiuntivi del servizio, come il monitoraggio, la risposta automatica e l'assicurazione.|
 {: caption="Tabella 1. Opzioni server aggiuntive" caption-side="top"}

## Configurazione di sistema avanzata
{: #adv-system-config}

I campi in **Configurazione di sistema avanzata** completano il tuo processo di provisioning.

| **Campo** | **Descrizione** |
|---|---|
| Nome host | Un nome permanente o temporaneo per il tuo server, ad esempio _server1_. **Nota**: se stai eseguendo il provisioning di un server con certificazione SAP, il tuo nome host SAP deve essere composto da un massimo di 13 caratteri alfanumerici. Per ulteriori informazioni sui nomi host SAP, vedi le note SAP [611361](https://launchpad.support.sap.com/#/notes/2611361) e [129997](https://launchpad.support.sap.com/#/notes/129997). Richiede un ID S-user SAP. |
| Dominio | Il nome del dominio secondario che non deve essere in conflitto con un nome di dominio Internet, ad esempio _test.acme.com_. |
| Selezione VLAN | Se c'è una VLAN nel tuo account perché già hai ordinato almeno un server, puoi aggiungere il nuovo server a tale VLAN.|
| Script di provisioning |Puoi fornire uno script che ti consente di automatizzare alcune operazioni dopo il provisioning. |
| Chiavi SSH | Puoi fornire la chiave pubblica della tua chiave SSH, che ti consentirà di accedere al tuo server dopo che ne è stato eseguito il provisioning. |
{: caption="Tabella 2. Configurazione di sistema avanzata" caption-side="top"}

 Consulta il supporto {{site.data.keyword.cloud_notm}} per ulteriori informazioni.

 **NOTA:** puoi ordinare delle sottoreti secondarie con i tuoi dispositivi di calcolo. Tuttavia, se ordini delle sottoreti secondarie, vengono recuperate quando viene recuperato il dispositivo di calcolo. Se ordini la sottorete secondaria indipendentemente (non come un'opzione di componente aggiuntivo di un ordine di calcolo), puoi conservare la sottorete finché non la annulli esplicitamente. È importante ricordare questa distinzione, così non perdi inavvertitamente qualche indirizzo IP se viene recuperato un dispositivo di calcolo.

## Passi successivi
Dopo che è stato eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}}, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione di {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
