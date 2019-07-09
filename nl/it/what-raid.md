---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: raid, about raid

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Informazioni su RAID
{: #bm-raid-levels}

RAID (Redundant Array of Independent Disks) crea un singolo disco di dati utilizzabile in cui diversi dischi fisici vengono combinati in un array per una migliore velocità e tolleranza di errore. Di seguito sono riportati i tre concetti chiave in RAID:
* **Mirroring**: copia dei dati in più di un disco
* **Striping**: suddivisione dei dati su più di un disco
* **Correzione degli errori** (tolleranza di errore): vengono memorizzati dei dati ridondanti per consentire il rilevamento e l'eventuale correzione dei problemi.

Sebbene esistano molti livelli diversi di RAID, {{site.data.keyword.IBM_notm}} sceglie di supportare i tipi RAID più comuni: 0, 1, 5, 6 e 10. I diversi livelli di RAID utilizzano una o più delle seguenti tecniche, a seconda dei requisiti di sistema. Lo scopo principale dell'utilizzo di RAID è quello di migliorare l'affidabilità utilizzando SATA Raid 3Ware 9550SX o un controller RAID SA-SCSI Adaptec per tutte le soluzioni RAID distribuite.

RAID non è una soluzione di backup. Piuttosto, RAID crea un singolo disco di dati utilizzabile, in cui diversi dischi fisici vengono combinati in un array per una migliore velocità e tolleranza di errore.
{: note}

**RAID 0** (Striped set senza parità / Array non ridondante) implementa lo striping dei dati, in cui i blocchi di file vengono scritti su più dischi in frammenti che richiedono un minimo di due dischi. Il vantaggio di un RAID 0 è che la velocità di lettura/scrittura è aumentata notevolmente. Maggiore è il numero di dischi nell'array, maggiore è la larghezza di banda. Lo svantaggio di un RAID 0 è che non ha tolleranza di errore. Se una singola unità non funziona, l'array si interrompe. Inoltre, RAID 0 non implementa il controllo degli errori. Pertanto, qualsiasi errore è anche irreversibile. Una soluzione comune per la tolleranza di errore consiste nel disporre di un'unità esterna all'array che viene utilizzata come archiviazione di backup in caso di errore hardware.

**RAID 1** (Mirrored set senza parità) implementa il mirroring di dati. I dati vengono duplicati su 2 o 4 dischi tramite un controller raid hardware, fornendo così un certo grado di tolleranza di errore. L'array è recuperabile se almeno un'unità non è malfunzionante. Fornisce prestazioni di lettura più veloci rispetto a una singola unità e fornisce ridondanza dell'unità in caso di errore dell'unità. La velocità di scrittura è leggermente ridotta.

**RAID 5** (Striped set con parità distribuita duale) implementa lo striping dei dati a livello di blocco e distribuisce la parità tra i dischi. Le informazioni di parità consentono il ripristino dall'errore di qualsiasi singola unità perché le eventuali letture successive possono essere calcolate dalla parità distribuita. RAID 5 consente inoltre una maggiore velocità di lettura/scrittura e consente l'uso più efficiente dello spazio su disco. RAID 5 richiede un minimo di tre dischi.

**RAID 6** (Doppia parità) implementa stripe con doppia parità su ciascun disco e consente l'errore su due dischi prima che i dati vengano persi. Poiché RAID 6 ha una capacità di due unità disco dedicate alla memorizzazione dei dati di parità in una serie di parità, si verificano maggiori operazioni di I/O con RAID 6 rispetto a RAID 5. Queste maggiori operazioni di I/O possono ridurre le prestazioni. RAID 6 richiede un minimo di 4 dischi e un massimo di 18 dischi.

**RAID 10** (RAID 1 + 0) Crea più mirror, dove i dati vengono organizzati come stripe su più dischi e quindi viene eseguito il mirroring dei set di dischi in striping. RAID 10 offre la stessa tolleranza di errore di RAID 1 con velocità di lettura/scrittura aumentate rispetto a una singola unità o un singolo volume Raid 1. RAID Level 10 richiede quattro dischi da implementare.
