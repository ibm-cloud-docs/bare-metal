---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selezione dai server più popolari
{: #bm-select-popular-servers}

I server nell'elenco dei server più popolari sono preconfigurati per soddisfare le esigenze della maggior parte dei casi di utilizzo del client e sono pronti in 30 - 40 minuti dopo averli ordinati.
1. Apri il [Catalogo {{site.data.keyword.cloud_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/catalog/){: new_window}.   
2. Seleziona Bare Metal Server.
3. Fai clic su Continua.  Se non visualizzi un pulsante Continua, potresti dover eseguire l'accesso.
2. Nella sezione {{site.data.keyword.baremetal_short}}, seleziona le seguenti informazioni:
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
    <td>Quantità </td>
    <td>Utilizza le icone + e - per specificare il numero di server **identici** di cui eseguire il provisioning. Il valore predefinito è 1.<br>Se vuoi eseguire il provisioning di più server con **diverse** specifiche, devi eseguirne il provisioning separatamente.<tr>
    <tr>
    <td>Tipo di fatturazione</td>
    <td>Seleziona oraria o mensile
    <tr>
    <td>Nome host e dominio</td>
    <td>Questi campi vengono popolati con l'impostazione predefinita. Puoi modificarli.</td>
    </tr>
    <tr>
    <td>Ubicazione</td>
    <td>Seleziona la regione in cui desideri ubicare il server. Utilizzando l'elenco a discesa, seleziona il data center nella regione. </td>
    </tr>
    <tr>
    <tr>
    <td>Seleziona il tuo server</td>
    <td>Seleziona **Server popolari** e seleziona il server che soddisfa le tue esigenze. Questi server sono preconfigurati e pronti per l'utilizzo in 30 - 40 minuti.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Per impostazione predefinita si basa sul server selezionato.</td>
    </tr>
    <tr>
    <td>Chiavi SSH</td>
    <td>Fornisci una chiave pubblica della tua chiave SSH, che utilizzi per accedere al tuo server dopo che ne è stato eseguito il provisioning.</td>
    </tr>
    <tr>
    <td>Immagine <br>(Sistema operativo)</td>
    <td>Seleziona il sistema operativo per il server. Le tue opzioni di immagine possono essere limitate in base al server selezionato.</td>
    </tr>
    <td>Componenti aggiuntivi</td>
    <td>Espandi la sezione Componenti aggiuntivi per selezionare le opzioni appropriate o utilizzare i valori predefiniti./td>
    </tr>
    </TBODY>
    </table>
3. Nella sezione Dischi di archiviazione, il disco di archiviazione è già selezionato per la tua selezione di server popolari. Espandi la sezione Componenti aggiuntivi se vuoi aggiungere IBM Cloud Backup al tuo server.
4. Nella sezione Interfaccia di rete, seleziona le Velocità porta di uplink. Espandi la sezione Componenti aggiuntivi per selezionare le opzioni appropriate o utilizzare i valori predefiniti. 
4.  Riesamina il tuo ordine. 
4. Se hai un codice promozionale da applicare al tuo ordine, espandi Applica codice promozionale.  
5.  Riesamina tutti gli accordi di servizio di terze parti elencati e fai clic sulla casella di spunta **Accordo di servizio di terze parti**.
6.  Fai clic su **Provisioning**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

 Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning.

 L'_email di completamento del provisioning_ include un link alla tua pagina *Dettagli dispositivo* in modo che puoi accedere a {{site.data.keyword.cloud_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.


## Passi successivi

Dopo che è stato eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}}, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione di {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
