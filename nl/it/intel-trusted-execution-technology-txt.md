---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Controlli di monitoraggio e sicurezza dell'hardware

L'escalation e la sofisticatezza delle minacce con intenti malevoli ti costringe ad adottare requisiti di sicurezza più rigidi e a controllare con attenzione ogni aspetto del tuo ambiente di sicurezza. Desideri che i tuoi fornitori cloud offrano controlli di monitoraggio e sicurezza dell'hardware che possano determinare se un carico di lavoro è in esecuzione su hardware affidabile in una località nota. {{site.data.keyword.cloud}} in questo è all'avanguardia e ti consente di distribuire ambienti ibridi e cloud con una verifica della sicurezza migliorata del tuo ambiente di avvio utilizzando Intel&reg; TXT (&reg; Trusted Execution Technology).
{:shortdesc}

## Come funziona

Intel TXT fornisce controlli di monitoraggio e sicurezza dell'hardware che aiutano a garantire alle attività commerciali che un carico di lavoro distribuito o migrato all'infrastruttura {{site.data.keyword.cloud_notm}} sia in esecuzione su hardware attendibile in una località nota. {{site.data.keyword.cloud_notm}} supporta Intel TXT su una gamma di {{site.data.keyword.baremetal_short}}. Vedi http://www.softlayer.com/intel-txt per un elenco completo.

Intel TXT analizza e misura i componenti di un sistema di elaborazione dal sistema operativo o dall'hypervisor all'hardware e al firmware di avvio del sistema di elaborazione. L'analisi include il BIOS (Basic Input/Output System) del sistema, l'MBR (Record di avvio principale, Master Boot Record) e il caricatore d'avvio. Le misurazioni vengono messe a confronto a una baseline standard per determinare se il sistema è attendibile o meno. Il software di sistema e il software di gestione locale o remoto può utilizzare la decisione di attendibilità per consentire o negare l'esecuzione di un carico di lavoro su tale sistema di elaborazione. Poiché Intel TXT esegue l'analisi e la misurazione durante l'avvio, la sicurezza aggiunta non aggiunge alcun sovraccarico delle prestazioni alle applicazioni.

Le misurazioni della baseline sono memorizzate su un dispositivo hardware TPM (Trusted Platform Module). Il dispositivo TPM viene integrato con il sistema server e fornisce una gamma di funzioni correlate alla sicurezza di Intel TXT.

## Cosa fa per te

Intel TXT è in particolar modo vantaggioso per le grandi aziende soggette a regolamenti di conformità e controllo, quali quelle operanti nel settore sanitario, quelle che si occupano di servizi finanziari e le organizzazioni governative. Aiuta a garantire che la traccia di tutte le risorse affidabili possa essere integrata, gestita e notificata con le organizzazioni di conformità pertinenti (HIPAA, PCI, FedRAMP, ISO, FISMA e SSAE 16). Per la prima volta, queste organizzazioni possono certificare che un sistema di elaborazione cloud è protetto in modo adeguato per carichi di lavoro quali

* Governance e rischio d'impresa
* Informazioni e gestione del ciclo di vita
* Conformità e controllo
* Sicurezza delle applicazioni
* Gestione di identità e accessi
* Risposta agli incidenti

Per ulteriori informazioni su Intel TXT su {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}, visita http://www.softlayer.com/intel-txt.

Il seguente link offre ulteriori informazioni sull'aggiunta di sicurezza e conformità maggiori ai tuoi carichi di lavoro con una [soluzione cloud sicura attendibile con IBM, VMware e HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf).

**Avviso tecnico speciale** Intel TXT (Trusted Execution Technology) è fornito da Intel&reg; e opera sui {{site.data.keyword.baremetal_short}} {{site.data.keyword.cloud_notm}} che richiedono una specifica competenza tecnica per il supporto e la gestione. Il modello di fornitura corrente di {{site.data.keyword.cloud_notm}} può attivare o disattivare Intel TXT; **{{site.data.keyword.cloud_notm}} non può assistere con la configurazione delle impostazioni di Intel TXT in ragione della riservatezza degli ambienti e dei dati dei clienti**. Ti consigliamo di includere del personale formato nelle tecnologie Intel TXT o di rivolgerti a una società di consulenza con una provata esperienza nell'orchestrazione dell'architettura MLE (measured launch environment) e della radice di attendibilità.
