---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# Opzione di nessun sistema operativo
{: #bm-no-os}

**Nessun sistema operativo** è un'opzione per ordinare {{site.data.keyword.baremetal_long}} senza un sistema operativo.

## Ordinazione di {{site.data.keyword.baremetal_short}} senza sistema operativo
{: #ordering-no-os}

1. Utilizza la procedura illustrata in [Creazione di un server bare metal personalizzato](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) per ordinare il tuo server.
2. Seleziona **Nessun sistema operativo** sotto **Immagine**.
3. Completa il tuo ordine del server. 

## Passaggio a nessun sistema operativo
{: #changing-to-no-os}

Un server può essere riconfigurato per non avere alcun sistema operativo. La riconfigurazione viene eseguita tramite un ricaricamento del sistema operativo. Per ulteriori informazioni, vedi [Ricaricamento del SO](/docs/infrastructure/software?topic=software-reloading-the-os).

1. Fai clic su **Dispositivi** > **Elenco dispositivi**.
2. Seleziona il server che deve essere riconfigurato senza sistema operativo.
3. Fai clic su **Ricaricamento SO** e immetti le informazioni applicabili.

## Installazione di un sistema operativo su un server senza sistema operativo
{: #installing-os-on-no-os-server}

Esistono due metodi per installare i sistemi operativi su {{site.data.keyword.baremetal_short}} senza sistema operativo.

### Opzione 1: server PXE
{: #option-1}

I {{site.data.keyword.baremetal_short}} senza sistemi operativi possono essere configurati per avviare e caricare un sistema operativo da una configurazione PXE.<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> Distribuisci i {{site.data.keyword.baremetal_short}} in un ambiente di rete con una configurazione PXE (ciò comporta di solito l'esecuzione di un daemon DHCP e TFTP) e configura il BIOS dei nuovi server per l'avvio dall'adattatore di rete. Affinché l'opzione di nessun sistema operativo funzioni correttamente, la configurazione PXE deve trovarsi nella stessa VLAN dei {{site.data.keyword.baremetal_short}} o deve essere utilizzato l'inoltro DHCP.

Potrebbe essere necessario aprire un ticket di supporto per richiedere che le porte di switch vengano raggruppate nuovamente in modalità di base affinché questa opzione funzioni. Ciò è dovuto al fatto che il protocollo PXE non richiede compatibilità con l'aggregazione di link (LACP), <!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> che ora è una funzionalità standard per fornire ridondanza. Un'altra opzione consiste nell'ordinare il server con uplink non associati (nessuna aggregazione di link) e quindi modificarli in uplink ridondanti dopo l'installazione del sistema operativo.
{: note}

### Opzione 2: dispositivo IPMI
{: #option-2}

Installa i sistemi operativi sui {{site.data.keyword.baremetal_short}} senza sistemi operativi eseguendo l'avvio da una ISO tramite il dispositivo IPMI incluso. Per ulteriori informazioni sull'avvio da una ISO, vedi [Montaggio di una ISO su un server bare metal](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server).
