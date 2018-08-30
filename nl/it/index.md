---



copyright:
  years: 2018, 2018
lastupdated: "2018-06-18"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introduzione ai server Bare Metal
{: #getting-started}

I {{site.data.keyword.baremetal_long}} sono server fisici a singolo tenant che ti forniscono prestazioni e controllo con un accesso di basso livello alle risorse hardware. Il tuo server non è condiviso con "vicini rumorosi"; è tutto tuo.
{: shortdesc}

La tabella 1 contiene i passi per aiutarti nel provisioning e nella configurazione dei tuoi {{site.data.keyword.baremetal_short}} in tempi brevi.
<table>
   <CAPTION>Tabella 1. Passi di avvio rapido</CAPTION>
   <THEAD>
   <TR>
   <th>Attività</th>
   <th>Dettagli</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. Riesamina il contenuto che può essere di aiuto con tua implementazione</td>
   <td>Non hai dimestichezza con IBM Cloud e i server bare metal? Questi siti ti forniscono informazioni utili per aiutarti a pianificare il tuo ambiente.
   <li><a href="https://ibm.com/cloud-computing/">Cos'è IBM Cloud</a></li>
   <li><a href="https://ibm.com/cloud/get-started">Introduzione a IBM Cloud</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Server Bare Metal</a></li>
   </td>
 <tr>
   <td>2. Registrati per IBM Cloud</td>
   <td><a href="https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-ibm-cloud">Signing up for IBM Cloud</a> contiene la procedura su come configurare il tuo account IBM Cloud.</td>
 <tr>
   <td>3. Determina le tue specifiche di carico di lavoro</td>
   <td>Prima di eseguire il provisioning del tuo server, determina come verrà utilizzato e la dimensione del server di cui hai bisogno per una soluzione vincente. Ad esempio, intendi utilizzarlo per lo sviluppo e l'attività di test oppure per la produzione? Stai testando un'esperienza utente, elaborando lunghi algoritmi, eseguendo il backup e il ripristino di dati o aumentando la velocità di latenza?</td>  
 <tr>
   <td>4. Definisci la dimensione e il costo del tuo server</td>
   <td>Puoi utilizzare lo <a href="https://www.ibm.com/cloud-computing/bluemix/bare-metal-search">strumento di ricerca bare metal</a> per un ausilio nella determinazione di dimensione e costo del tuo server.</td>
 <tr>
   <td>5. Esegui l'accesso al tuo account IBM Cloud</td>
   <td>Puoi accedere al modulo di ordine di Bare Metal Server dal catalogo IBM Cloud o dal portale clienti dell'infrastruttura IBM Cloud. Hai bisogno di <a href="https://console.bluemix.net/docs/customer-portal/getting-started.html#getting-started">un ID IBM e una password</a> per accedere al catalogo e al portale clienti dell'infrastruttura.
   <li><a href="https://console.bluemix.net/catalog/">Catalogo IBM Cloud</a></li>
   <li><a href="https://control.softlayer.com">Portale clienti dell'infrastruttura IBM Cloud</a></li>  
   </td>   
<tr>   
   <td>6. Esegui il provisioning del tuo server</td>
   <td>Quando si tratta di eseguire il provisioning del tuo server, hai tre opzioni: popolari, personalizzati e con certificazione SAP. I server popolari sono dei server preconfigurati che soddisfano le esigenze della maggior parte dei clienti e possono essere pronti da configurare 30 o 40 minuti dopo il provisioning. 
   
     
<br>I server personalizzati sono i server che crei selezionando specifiche opzioni di calcolo, connettività, archiviazione e rete per rispondere alle tue esigenze. Nota: il provisioning dei server personalizzati richiede più tempo, di norma dalle 2 alle 4 ore, e hanno dei costi operativi più elevati. Disponi anche dell'opzione di <a href="bm_provision_ssd.html">eseguire il provisioning di un server bare metal compatibile con Intel Optane</a> oppure di uno con un'<a href="bare-metal-provision-SGX.html">architettura Intel SGX</a>. 
     
<br>I server con certificazione SAP sono stati specificamente certificati per supportare landscape SAP HANA e SAP NetWeaver.
Utilizza i link per andare alle informazioni di provisioning per tale tipo di server. Nota: con i server con certificazione SAP, devi selezionare di quale tipo di landscape, SAP HANA o SAP NetWeaver, stai eseguendo il provisioning.  
  <li><a href="baremetal-provision-popular.html">Server bare metal con provisioning veloce</a></li>
  <li><a href="baremetal-provision.html">Server bare metal personalizzati</a></li>
  <li><a href="bare-metal-sap-applications.html">IBM Cloud SAP-Certified Infrastructure</a></li>
  </td>
 <tr>
   <td>7. Configura il tuo server bare metal</td>
   <td>Il tuo server è ora pronto per essere configurato. Vedi gli argomenti in *Configurazione*.</td>
   </td>
   </tr>
   </TBODY>
   </table>
