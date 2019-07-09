---

copyright:
  years:  2019
lastupdated: "2019-02-01"

keywrods: provision managed pool, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning di pool gestiti dal cliente
{: #bm-provision-managed-pools}

Per eseguire il provisioning di un pool di server gestito dal cliente, contatta direttamente IBM: [Come ottenere aiuto e supporto](/docs/bare-metal?topic=bare-metal-gettinghelp).

Fornisci le seguenti informazioni:
* Il data center in cui vuoi ubicare i tuoi pool gestiti. (Tutti i server in un pool gestito devono essere ubicati nello stesso data center.)
* Il numero di server che vuoi nel tuo pool gestito
* Le specifiche di cui hai bisogno per i tuoi server nel pool

Una volta creato il pool, IBM ti fornisce i seguenti valori di parametro. Hai bisogno di questi valori quando invii il comando API per gestire il tuo pool.
* poolKeyName
* backendRouter

## Ordinazione di server dal tuo pool gestito
{: #bm-order-server-managed-pool}
Utilizza il processo di provisioning standard per ordinare i server nel tuo pool. Il tuo ordine viene eseguito dal tuo pool e il pool viene rifornito con il numero di server che hai ordinato.

## Passi successivi

Dopo aver eseguito il provisioning del tuo pool gestito dal cliente e ordinato i server dal pool gestito, puoi gestire il numero di server presenti nel pool. Fai riferimento a [Specifica del numero di server nel tuo pool gestito dal cliente](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)
