---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Creazione di un Bare Metal Server personalizzato
{: #ordering-baremetal-server}

Utilizza la seguente procedura per creare un {{site.data.keyword.baremetal_long}} personalizzato.

## Provisioning tramite il catalogo {{site.data.keyword.cloud_notm}} 
{: #provision-through-the-catalog}

Utilizza la seguente procedura per eseguire il provisioning del tuo {{site.data.keyword.baremetal_short}} tramite {{site.data.keyword.cloud_notm}}.

1. Apri il [Catalogo {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog/){: external}.   
2. Seleziona {{site.data.keyword.baremetal_short}} in **Calcola**.
3. Fai clic su Continua.  Se non visualizzi un pulsante Continua, potresti dover eseguire l'accesso.
4. Immetti una **Quantità** di server **identici** per il provisioning. Il valore predefinito è 1. Se vuoi eseguire il provisioning di più server con _diverse_ specifiche, devi eseguire il provisioning dei server separatamente.
5. **Nome host** è un nome permanente o temporaneo per i tuoi server, ad esempio, baremetal01. Fai clic su **Informazioni** per la formattazione delle specifiche.
6. **Dominio** è la stringa di identificazione che definisce il controllo amministrativo in internet, ad esempio, Customer-123456.cloud. Fai clic su **Informazioni** per la formattazione delle specifiche.
7. **Fatturazione** è **Oraria** o **Mensile**.
8. Seleziona **Ubicazione**, regione e data center, in cui deve essere posizionato il tuo server.
9. Fai clic su **Tutti i server** per visualizzare l'elenco di processori (singolo, duale e quadruplo) e i server certificati (SAP e VMware). Seleziona il server che meglio si adatta al tuo carico di lavoro.
10. Seleziona la tua **RAM**. Per alcuni server, la RAM per impostazione predefinita si basa sul modello di CPU e non può essere modificata. 

Per i server certificati SAP, la RAM e il sistema operativo per impostazione predefinita si basano sulla tua selezione del server. Anche la tua opzione di archiviazione locale per impostazione predefinita si basa sulla tua selezione del server.
{ :note}

11. Immetti una chiave pubblica facoltativa per la tua **chiave SSH**, che puoi utilizzare per accedere al tuo server dopo che ne è stato eseguito il provisioning.
12. Seleziona un'**Immagine** (sistema operativo) per il tuo server. Le tue opzioni si basano sulla tua selezione del server.
13. Espandi **Componenti aggiuntivi** per selezionare le opzioni correlate alla configurazione del server.
14. I **Dischi di archiviazione** vengono preconfigurati in base alla tua selezione del server. Espandi **Componenti aggiuntivi** per aggiungere dei volumi di archiviazione file o blocchi dopo aver eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}}. 
15. In **Interfaccia di rete**, seleziona le opzioni Velocità porta di uplink e VLAN privata. Espandi **Componenti aggiuntivi** per selezionare le opzioni appropriate o utilizzare i valori predefiniti.
16. Riesamina il tuo ordine nel Riepilogo ordine.
17. Immetti tutti i codici promozionali di cui disponi in **Applica codice promozionale**.
18. Fai clic sugli accordi di servizio di terze parti per tutti gli accordi elencati.
19. Fai clic su **Crea** per eseguire il provisioning del tuo server. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning, che puoi stampare perché è anche la tua ricevuta.

Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning.

L'email di _completamento del provisioning_ include un link alla tua pagina *Dettagli dispositivo* in modo che puoi accedere a {{site.data.keyword.cloud_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

Hai anche l'opzione di salvare l'ordine come una quota o di aggiungerlo a una stima. Quando salvi una quota, viene inviato un link all'indirizzo email associato al tuo account. Apri il link per visualizzare le informazioni sulla quota salvata. Un'altra opzione è di andare a Gestisci > Fatturazione e utilizzo e selezionare Vendite > Quote dispositivo. Se hai accesso puoi acquistare l'offerta quotata facendo clic sulla quota e confermando l'ordine. L'aggiunta della stima inserisce il costo proposto per le configurazioni nel calcolatore del prezzo. Fai clic su **Informazioni** per ulteriori dettagli sul calcolatore del prezzo.

## Provisioning tramite il portale clienti
Utilizza la seguente procedura per eseguire il provisioning del tuo {{site.data.keyword.baremetal_short}} tramite {{site.data.keyword.slportal}}.

1. Accedi a [{{site.data.keyword.slportal}}](control.softlayer.com){: external} utilizzando le tue credenziali univoche.
2. Vai a **Account** > **Place an Order**.
3. Scegli **Hourly** o **Monthly**.
3. Seleziona il tuo data center in cui vuoi sia posizionato il tuo {{site.data.keyword.baremetal_short}} dall'elenco e poi seleziona il tuo server certificato (SAP o VMware) o processore (singolo, duale o quadruplo) facendo clic su **STARTING PRICE**.
4. Immetti una **Quantità** di server _identici_ per il provisioning. Il valore predefinito è 1. Se vuoi eseguire il provisioning di più server con _diverse_ specifiche, devi eseguire il provisioning dei server separatamente.
5. Seleziona la tua **RAM**. Per alcuni server, la RAM per impostazione predefinita si basa sul modello di CPU e non può essere modificata. 

Per i server certificati SAP, la RAM e il sistema operativo per impostazione predefinita si basano sulla tua selezione del server. Anche la tua opzione di archiviazione locale per impostazione predefinita si basa sulla tua selezione del server.
{ :note}

6. Seleziona il tuo sistema operativo.
7. Seleziona i tuoi dischi rigidi e componenti aggiuntivi del sistema.
8. Fai clic su **Add to Order** da cui vieni reindirizzato per confermare il tuo ordine.
9. Conferma o modifica le informazioni sul dominio per il server. **Nome host** è un nome permanente o temporaneo per i tuoi server, ad esempio, baremetal01.  
10. Seleziona **Cloud Service terms** e **Third-Party Service Agreement**.
11. Immetti tutti i codici promozionali di cui disponi in **Promo code** e fai clic su **Apply**.
12. Conferma o immetti le informazioni di pagamento e fai clic su **Submit Order**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning, che puoi stampare perché è anche la tua ricevuta. 

Una serie di email viene inviata al tuo amministratore: il riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione dell'ordine di provisioning e il completamento del provisioning. L'email di completamento del provisioning include un link alla tua pagina *Dettagli dispositivo* dopo l'esecuzione dell'accesso a {{site.data.keyword.Bluemix_notm}}. Puoi anche accedere direttamente al {{site.data.keyword.slportal}}.

## Passi successivi
Dopo che è stato eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}}, puoi iniziare a gestirlo. Per ulteriori informazioni, vedi [Gestione di {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
