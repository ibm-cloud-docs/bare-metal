---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurazione del tuo server bare metal

È una buona idea dedicare tutto il tempo necessario a prendere le proprie decisioni di configurazione prima dell'esecuzione del provisioning del tuo {{site.data.keyword.baremetal_long}}. Questo rende il processo di provisioning più rapido e fluido.{:shortdesc}

## Determinazione dell'uso del server e delle sue dimensioni

La tua prima attività consiste nel determinare come userai il tuo {{site.data.keyword.baremetal_short}}. Ad esempio, intendi utilizzarlo per attività di sviluppo/test o produzione? Stai testando un'esperienza utente, elaborando lunghi algoritmi, eseguendo il backup e il ripristino di dati o aumentando la velocità di latenza?

Dopo che hai determinato come deve essere utilizzato il tuo {{site.data.keyword.baremetal_short}}, devi stabilirne le dimensioni. La [calcolatrice del costo totale di proprietà di SoftLayer](http://www.softlayer.com/tco/) può aiutarti a determinare quale {{site.data.keyword.baremetal_short}} risponde meglio alle tue esigenze.

## Selezione del tuo server

{{site.data.keyword.cloud_notm}} offre sette server con una rapida procedura di provisioning per garantire che tu abbia le prestazioni di cui hai bisogno per il tuo carico di lavoro. Questi server sono attualmente disponibili nelle regioni Regno Unito e Stati Uniti Sud.

| **Configurazione** | **Processore** | **Memoria** | **Disco rigido** | **Velocità della porta** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 core, 3,50 GHz) |32 GB di RAM |1 unità disco rigido interna |Velocità di porta massima di 100 Mbps|
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3 (6 core, 2,40 GHz) |64 GB di RAM |2 unità disco rigido interne |Velocità di porta massima di 100 Mbps|
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 core, 3,50 GHz) |32 GB di RAM |2 unità disco rigido interne |Velocità di porta massima di 100 Mbps|
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3 (10 core, 2,30 GHz) |128 GB di RAM |1 unità disco rigido interna |Velocità di porta massima di 100 Mbps|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 core, 2,60 GHz) |128 GB di RAM |2 unità disco rigido interne |Velocità di porta massima di 100 Mbps|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 core, 2,60 GHz) |64 GB di RAM |4 unità disco rigido interne |Velocità di porta massima di 1.000 Mbps|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 core, 2,60 GHz) |256 GB di RAM |4 unità disco rigido interne |Velocità di porta massima di 1.000 Mbps|

Oltre ai sette server con una rapida procedura di provisioning, {{site.data.keyword.cloud_notm}} ha ampliato la sua offerta di {{site.data.keyword.baremetal_short}} per includere i sistemi bare metal basati su POWER8. Questi sistemi sono sviluppati con il processore POWER8 {{site.data.keyword.IBM_notm}} e una piattaforma basata su OpenPower regolata in modo mirato per le distribuzioni basate sul cloud di carichi di lavoro web, cognitivi e di dati su Linux.

È possibile eseguire un upgrade di tutti i {{site.data.keyword.baremetal_short}} per includere una larghezza di banda illimitata. Tutti i dispositivi illimitati sono su porte private e dedicate.

## Configurazione dei tuoi server bare metal

Dopo che hai selezionato il tuo data center, il tuo server e l'opzione di fatturazione (mensile od oraria), devi decidere come configurare il tuo server. Alcuni campi (Server, RAM, GPU (Graphics Processing Unit) e GPU (Graphics Processing Unit) secondaria) nella pagina **Configura il tuo {{site.data.keyword.baremetal_short}}** saranno impostati automaticamente sulla base della tua selezione del server. La seguente tabella descrive i campi per cui puoi definire un valore.

| **Campo** | **Descrizione** | 
|-------------------|---------------|
|Sistema operativo |Seleziona da CentOS, FreeBSD, Microsoft, Red Hat, Unbuntu o Altro. |
|Dischi rigidi |Lo strumento di configurazione del disco ti aiuta a configurare i tuoi dischi rigidi precompilando i campi in base alla tua selezione del sistema operativo. |
|Larghezza di banda pubblica |Determina la quantità di dati che può essere trasferita tramite l'interfaccia pubblica nel corso di un mese. Per gli ambienti di test, che richiedono dati di installazione trasferiti tramite questa interfaccia, i valori devono essere adattati oltre la quantità di dati trasferita inizialmente. Sarebbe opportuno che tu prendessi in considerazione la [Content Delivery Network {{site.data.keyword.cloud_notm}}](https://www.ibm.com/cloud/cdn) per fornire un carico di dati iniziale a uno dei data center {{site.data.keyword.cloud_notm}}. |
|Velocità porta di uplink |Determina la velocità delle interfacce interne ed esterne. |
|Indirizzi IP secondari pubblici |Assegna un indirizzo IP aggiuntivo al tuo server. A seconda del tuo scenario, potresti aver bisogno di ulteriori indirizzi IP assegnati al tuo server. Degli indirizzi IPv4 aggiuntivi sono disponibili in quantità di 1, 2, 4, 8, 16 o 32. |
|Indirizzi IPv6 primari |Assegnati alle interfacce interne e a quelle esterne del tuo server. |
|Indirizzi IPv6 statici pubblici |Assegna ulteriori indirizzi IPv6 da un blocco /64. |
|Firewall hardware e software, Protezione antivirus e spyware e Rilevamento e prevenzione delle intrusioni. |Seleziona le opzioni appropriate se il server interagisce con Internet. Ti consigliamo vivamente di allineare il tuo dipartimento di sicurezza aziendale con il supporto {{site.data.keyword.cloud_notm}} per discutere i dettagli di queste opzioni. |
|Evault |Uno strumento di backup basato sugli agent che può essere installato sul tuo server per replicare i backup tra i server. |

Per ulteriori informazioni, consulta [Design Decision Tool](http://knowledgelayer.softlayer.com/learning/softlayer-design-decision-tool) oppure il supporto {{site.data.keyword.cloud_notm}}.


## Configurazione di sistema avanzata

La configurazione di sistema avanzata viene eseguita dopo che hai fatto clic sul pulsante **Aggiungi all'ordine** e che sei stato reindirizzato alla pagina Checkout. La seguente tabella descrive i campi nella configurazione di sistema avanzata.

| **Campo** | **Descrizione** | 
|-------------------|---------------|
|Nome host |Un nome permanente o temporaneo per il tuo server, ad esempio _server1_. |
|Dominio |Il nome del dominio secondario che non deve essere in conflitto con un nome di dominio Internet, ad esempio _test.acme.com_. |
|Selezione VLAN |Se c'è una VLAN sotto al tuo account perché già hai ordinato almeno un server, puoi aggiungere il nuovo server a tale VLAN. |
|Script di provisioning |Puoi fornire uno script che ti consente di automatizzare alcune operazioni dopo che è stato eseguito il provisioning del server. |
|Chiavi SSH |Puoi fornire una chiave pubblica per la tua chiave SSH, che ti consentirà di accedere al tuo server dopo che ne è stato eseguito il provisioning. |
