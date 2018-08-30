---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Opzione di nessun sistema operativo (No OS)

Nessun sistema operativo (No OS) è un'opzione per ordinare un server bare metal senza un sistema operativo.

## Come ordinare un server bare metal senza sistema operativo?

Inizia ordinando un server bare metal tramite [SoftLayer.com](https://www.softlayer.com) o il [Portale clienti](https://control.softlayer.com).

1. Seleziona **Altro** da **Configurazione di sistema > Sistema operativo**.
2. Seleziona **Nessun sistema operativo**.

## Come installare un sistema operativo su un server senza un sistema operativo?

Ci sono due metodi per installare un sistema operativo su un server bare metal senza un sistema operativo.

### Opzione 1: server PXE

Un server bare metal senza sistema operativo può essere configurato per eseguire l'avvio e il caricamento del sistema operativo da una configurazione PXE (vedi [Preboot Execution Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) per ulteriori informazioni). Distribuisci semplicemente il server bare metal in un ambiente di rete con una configurazione PXE (ciò comporta di norma l'esecuzione di un daemon DHCP e TFTP) e configura il BIOS del nuovo server bare metal per l'avvio dall'adattatore di rete. Perché l'opzione di nessun sistema operativo (No OS) funzioni correttamente, la configurazione PXE deve trovarsi nella stessa VLAN del server bare metal, altrimenti bisogna utilizzare l'inoltro DHCP.

**Nota:** potrebbe essere necessario aprire un ticket di supporto che richiede che le porte di switch vengano raggruppate nuovamente in modalità di base perché questa opzione funzioni. Ciò è dovuto al fatto che il protocollo PXE non richiede la compatibilità con l'aggregazione di link (ossia LACP; vedi [Link aggregation](http://en.wikipedia.org/wiki/Link_aggregation)), che è ora una funzionalità standard per fornire la ridondanza. Un'altra opzione consiste nell'ordinare il server con gli uplink non associati (nessuna aggregazione di link) e modificarli quindi in uplink ridondanti dopo che il sistema operativo è stato installato.

### Opzione 2: dispositivo IPMI

Installa un sistema operativo su un server bare metal senza un sistema operativo eseguendo l'avvio da una ISO tramite il dispositivo IPMI. Fai clic [qui](mount-iso-bare-metal-server.html) per ulteriori informazioni sull'avvio da una ISO.
