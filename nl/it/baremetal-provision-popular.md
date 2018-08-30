---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selezione dai server più popolari
I server nell'elenco Most Popular Servers sono preconfigurati per soddisfare le esigenze della maggior parte dei casi d'uso dei clienti e sono pronti per l'esecuzione in 30 - 40 minuti dopo che li hai ordinati.
1. Apri il catalogo [{{site.data.keyword.cloud_notm}}](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Seleziona Bare Metal Server.
3. Fai clic su Crea.
2. Seleziona le seguenti informazioni:
    <table>
    <CAPTION>Tabella 1. Selezioni bare metal</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valore</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantità</td>
    <td>Utilizza le icone + e - per specificare il numero di server identici di cui eseguire il provisioning. <br>Se vuoi eseguire il provisioning di più server con specifiche differenti, devi eseguirne il provisioning separatamente.
    <tr>
    <td>Ubicazione</td>
    <td>Seleziona la regione e il data center in cui desideri che il server sia ubicato.</td>
    </tr>
    <tr>
    <tr>
    <td>Nome host e Dominio</td>
    <td>Questi campi vengono compilati con il valore predefinito. Puoi modificarli.</td>
    </tr>
    <tr>
    <td>Seleziona il tuo server</td>
    <td>In **Server popolari**, seleziona il server che soddisfa le tue esigenze. Questi server sono preconfigurati e sono pronti per l'uso in 30 - 40 minuti.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Valore predefinito basato sul server da te selezionato.</td>
    </tr>
    <tr>
    <td>Chiavi SSH</td>
    <td>Fornisci una chiave pubblica della tua chiave SSH, che utilizzi per accedere al tuo server dopo che ne è stato eseguito il provisioning.</td>
    </tr>
    <tr>
    <td>Immagine<br>(Sistema operativo)</td>
    <td>Seleziona il sistema operativo per l'istanza. **Nota**: viene visualizzato un messaggio di errore se si verifica un conflitto tra il server e il sistema operativo. Un esempio è la selezione di Linux su un server Microsoft SQL.</td>
    </tr>
    <td>Velocità porta di uplink</td>
    <td>Determina la velocità delle interfacce interne ed esterne.</td>
    </tr>
    <tr>
    <td>Componenti aggiuntivi</td>
    <td> Seleziona le opzioni appropriate oppure utilizza i valori predefiniti.</td>
    </tr>
    </TBODY>
    </table>

3.  Nella sezione Order Summary, seleziona la fatturazione oraria (**Hourly**) o mensile (**Monthly**).
4.  Riesamina il tuo ordine.
5.  Riesamina gli eventuali accordi di servizio di terze parti elencati e fai clic sulla casella di spunta **Third-Party Service Agreement**.
6.  Fai clic su **Provision**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

 Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning. L'email di completamento del provisioning include un link alla tua pagina *Device Details* in modo da consentirti di eseguire l'accesso a {{site.data.keyword.cloud_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.


## Passi successivi
Dopo che è stato eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}}, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione di {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
