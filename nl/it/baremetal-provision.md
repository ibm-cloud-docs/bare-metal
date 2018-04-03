---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning del server bare metal

## Prima di iniziare
Hai due opzioni per eseguire il provisioning dli tuo {{site.data.keyword.baremetal_long}} pubblici. la prima è tramite il catalogo {{site.data.keyword.cloud}} e la seconda è tramite il {{site.data.keyword.slportal_full}}. Il catalogo e il {{site.data.keyword.slportal}} richiedono degli ID univoci. I tuoi nome utente e password del catalogo non funzioneranno per eseguire l'accesso al portale e viceversa.
{:shortdesc}

Prima di iniziare, assicurati che le tue credenziali per il catalogo {{site.data.keyword.cloud_notm}} o il {{site.data.keyword.slportal}} siano configurate. 
  
**Nota:** per il catalogo {{site.data.keyword.cloud_notm}}, devi disporre di un account di cui è stato eseguito l'upgrade per ordinare {{site.data.keyword.baremetal_short}}. Per ulteriori informazioni sull'esecuzione di un upgrade del tuo account, vedi il documento relativo al [passaggio all'ID IBM](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
## Accesso 
Assicurati di avere eseguito l'accesso, tramite il catalogo {{site.data.keyword.cloud_notm}} o {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Tabella 1. Scegli un'ubicazione di accesso</CAPTION>
   <THEAD>
   <TR>
   <th>Se vuoi accedere con...</th>
   <th>Allora...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catalogo IBM Cloud</td>
   <td>
   <ol>
   <li>Apri una nuova finestra del browser e immetti <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Fai clic sul link <b>Accedi</b>. </li>
   <li>Immetti la tua email o il tuo ID IBM e fai clic su <b>Continua</b>.</li>
   <li>Immetti la tua password e fai clic su <b>Accedi</b>.</li>
   <li>Seleziona <b>Infrastruttura</b> > <b>Calcola</b>.</li>
   <li>Fai clic sul tile <b>{{site.data.keyword.baremetal_short}}</b>.</li>
   <li>Fai clic su <b>Crea</b>. Viene visualizzata la pagina principale del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portale clienti</td>
   <td>
   <ol>
   <li>Apri una nuova finestra del browser e immetti <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Immetti i tuoi nome utente e password e fai clic su <b>Log In</b>. In alternativa, fai clic su <b>Log in with IBMid</b>. Immetti quindi la tua email o il tuo ID IBM e fai clic su <b>Continue</b>. Immetti la tua password e fai clic su <b>Log In</b>. Viene visualizzata la pagina principale del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisioning di un server bare metal
{: #ordering-baremetal-server}
Dopo che hai eseguito l'accesso, puoi iniziare a eseguire il provisioning di un {{site.data.keyword.baremetal_short}}. Puoi eseguire il provisioning del tuo {{site.data.keyword.baremetal_short}} tramite il menu **Dispositivi** o l'icona **Dispositivi**.

### Provisioning di un server bare metal tramite l'icona Dispositivi
Per eseguire il provisioning del tuo {{site.data.keyword.baremetal_short}} tramite l'icona *Dispositivi*, completa la seguente procedura:

1.  Dal {{site.data.keyword.slportal}}, individua la sezione **Ordine** e fai clic su **Dispositivi**.
2.  Nella pagina Dispositivi, fai clic su **Orario** o **Mensile** in {{site.data.keyword.baremetal_short}}.
3.  Seleziona il tuo **Data Center**, scorri la pagina e fai clic sul link **Prezzo di partenza per** per selezionare il tuo server. 
4.  Compila le informazioni nella pagina **Configura il tuo {{site.data.keyword.baremetal_short}}** e fai clic sul pulsante **Aggiungi all'ordine** per continuare. Vedi [Configurazione del tuo {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) per ulteriori informazioni su come configurare il tuo server. Dopo che il tuo ordine è stato verificato, verrai reindirizzato alla pagina **Checkout**.
5.  Accedi alla **Configurazione avanzata del sistema**) per il server. Vedi [Configurazione del tuo {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) per ulteriori informazioni su come eseguire questa configurazione.
6.  Fai clic sulle caselle di spunta **Termini del servizio cloud** e **Accordo servizi di terze parti**.
7.  Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Invia ordine**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

 Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning. L'email di completamento del provisioning include un link alla tua pagina *Dettagli dispositivo* dopo l'esecuzione dell'accesso a {{site.data.keyword.cloud_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

### Provisioning del server bare metal tramite il menu Dispositivi
{: #ordering-baremetal-devices-menu}

Puoi anche eseguire il provisioning del tuo {{site.data.keyword.baremetal_short}} tramite il menu *Dispositivi* nella pagina principale del {{site.data.keyword.slportal}}. 

1. Fai clic su **Dispositivi > Elenco dispositivi**. La pagina Dispositivi visualizza tutti i tipi di dispositivi - host dedicati, server virtuali, server bare metal e controller di distribuzione applicazione NetScaler, nel tuo account.
2. Fai clic sul link **Ordine dispositivi** nell'angolo superiore destro.
3. Nella pagina Ordina prodotti e servizi SoftLayer, fai clic su **Orario** o **Mensile** in {{site.data.keyword.baremetal_short}}.
4. Seleziona il tuo **Data Center**, scorri la pagina e fai clic sul link **Prezzo di partenza per** per selezionare il tuo server. 
5.  Compila le informazioni nella pagina **Configura il tuo {{site.data.keyword.baremetal_short}}** e fai clic sul pulsante **Aggiungi all'ordine** per continuare. Vedi [Configurazione del tuo {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) per ulteriori informazioni su come configurare il tuo server. Dopo che il tuo ordine è stato verificato, verrai reindirizzato alla pagina **Checkout**.
6.  Accedi alla **Configurazione avanzata del sistema**) per il server. Vedi [Configurazione del tuo {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) per ulteriori informazioni su come eseguire questa configurazione.
7. Fai clic sulle caselle di spunta **Termini del servizio cloud** e **Accordo servizi di terze parti**.
8. Conferma o immetti le tue informazioni di pagamento e fai clic sul pulsante **Invia ordine**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning. L'email di completamento del provisioning include un link alla tua pagina *Dettagli dispositivo* dopo l'esecuzione dell'accesso a {{site.data.keyword.cloud_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

### Passi successivi
Dopo che è stato eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}}, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione di {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
