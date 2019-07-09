---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-16"

keywords: bare metal, getting started, {{site.data.keyword.cloud}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Esercitazione introduttiva
{: #getting-started}

I {{site.data.keyword.baremetal_long}} sono server fisici a singolo tenant che ti forniscono prestazioni e controllo con un accesso di basso livello alle risorse hardware. Il tuo server non è condiviso con il contesto esterno; è tutto tuo.
{: shortdesc}

La tabella 1 contiene i passi per aiutarti nel provisioning e nella configurazione dei tuoi {{site.data.keyword.baremetal_short}} in tempi brevi.
<table>
   <CAPTION>Tabella 1. Procedura d'avvio rapida</CAPTION>
   <THEAD>
   <TR>
   <th>Attività</th>
   <th>Dettagli</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. Riesamina il contenuto che può essere di aiuto con la tua implementazione</td>
   <td>Non hai esperienza pregressa con IBM Cloud e i server bare metal? I seguenti siti forniscono informazioni utili per aiutarti a pianificare il tuo ambiente.
   <li><a href="https://ibm.com/cloud-computing/">Cos'è IBM Cloud</a></li>
   <li><a href="https://ibm.com/cloud/get-started">Introduzione a IBM Cloud</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Server bare metal</a></li>
   </td>
 <tr>
   <td>2. Registrati in IBM Cloud</td>
   <td><a href="https://cloud.ibm.com/docs/account?topic=account-signup#signing-up-for-ibm-cloud">Registrati in IBM Cloud</a> contiene i passi su come configurare il tuo account IBM Cloud.</td>
 <tr>
   <td>3. Determina le tue specifiche di carico di lavoro</td>
   <td>Prima di eseguire il provisioning del tuo server, determina come verrà utilizzato e la dimensione del server di cui hai bisogno per una soluzione vincente. Ad esempio, intendi utilizzarlo per lo sviluppo e l'attività di test oppure per la produzione? Stai testando un'esperienza utente, elaborando lunghi algoritmi, eseguendo il backup e il ripristino di dati o aumentando la velocità di latenza?</td>  
 <tr>
   <td>4. Definisci la dimensione e il costo del tuo server</td>
   <td>Puoi utilizzare lo <a href="https://cloud.ibm.com/gen1/infrastructure/provision/bm">strumento di ricerca bare metal</a> per un ausilio nella determinazione di dimensione e costo del tuo server.</td>
 <tr>
   <td>5. Esegui l'accesso al tuo account IBM Cloud</td>
   <td>Puoi accedere al modulo di ordine di Bare Metal Server dal catalogo IBM Cloud o dal portale clienti dell'infrastruttura IBM Cloud. Hai bisogno di un <a href="https://cloud.ibm.com/docs/customer-portal?topic=customer-portal-getting-started#getting-started">ID IBM e una password</a> per accedere al catalogo e al portale clienti dell'infrastruttura.
   <li><a href="https://cloud.ibm.com/catalog/">Catalogo IBM Cloud</a></li>
   <li><a href="https://cloud.ibm.com">Console IBM Cloud</a></li>  
   </td>   
<tr>   
   <td>6. Esegui il provisioning del tuo server</td>
   <td>Quando si tratta di eseguire il provisioning del tuo server, hai tre opzioni: provisioning veloce, personalizzato e con certificazione SAP. I server con provisioning veloce sono dei server preconfigurati che soddisfano le esigenze della maggior parte dei clienti e possono essere pronti da configurare 30 o 40 minuti dopo il provisioning.


<br>I server personalizzati sono i server che crei selezionando specifiche opzioni di calcolo, connettività, archiviazione e rete per rispondere alle tue esigenze. Il provisioning dei server personalizzati richiede più tempo, di norma dalle 2 alle 4 ore, e hanno dei costi operativi più elevati. Puoi [eseguire il provisioning di un server bare metal compatibile con Intel Optane](/docs/bare-metal?topic=bare-metal-provisioning-an-intel-optane-compatible-bare-metal-server#provisioning-an-intel-optane-compatible-bare-metal-server) o di uno con un'[architettura Intel SGX](/docs/bare-metal?topic=bare-metal-provisioning-a-bare-metal-server-with-intel-sgx-architecture#provisioning-a-bare-metal-server-with-intel-sgx-architecture).

<br>I server con certificazione SAP sono certificati per supportare landscape SAP HANA e SAP NetWeaver.
Utilizza i link per accedere alle informazioni di provisioning per tale tipo di server. Nota che con i server con certificazione SAP, devi selezionare il tipo di landscape, SAP HANA o SAP NetWeaver, di cui stati eseguendo il provisioning.<br>
* [Server bare metal con provisioning veloce](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers)<br>
* [Server bare metal personalizzati](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server#ordering-baremetal-server)<br>
* [IBM Cloud SAP-Certified Infrastructure](/docs/bare-metal?topic=bare-metal-ibm-cloud-sap-certified-infrastructure#ibm-cloud-sap-certified-infrastructure)
  </td>
 <tr>
   <td>7. Configura il tuo server bare metal</td>
   <td>Il tuo server è ora pronto per essere configurato. Vedi gli argomenti in **Configurazione**.</td>
   </td>
   </tr>
   </TBODY>
   </table>
