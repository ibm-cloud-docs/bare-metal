---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informazioni su RAID

RAID (Redundant Array of Independent Disks) crea un singolo disco di dati utilizzabile in cui diversi dischi fisici vengono combinati in un array per una velocità e una resistenza ai guasti migliorate. In RAID, i concetti chiave sono tre:
* Mirroring -- copia dei dati in più di un disco
* Striping -- suddivisione dei dati su più di un disco
* Correzione degli errori (tolleranza ai guasti) -- vengono memorizzati dei dati ridondanti per consentire il rilevamento ed eventualmente la correzione dei problemi. 

Anche se ci sono molti livelli differenti di RAID, IBM ha scelto di supportare i tipi di RAID più comuni: 0, 1, 5 e 10. I diversi livelli di RAID utilizzano una o più delle seguenti tecniche, a seconda dei requisiti di sistema. Lo scopo principale dell'utilizzo di RAID è quello di migliorare l'affidabilità utilizzando SATA Raid 3Ware 9550SX o un controller RAID SA-SCSI Adaptec per tutte le soluzioni RAID distribuite.

RAID non è una soluzione di backup. RAID crea un singolo disco di dati utilizzabile in cui diversi dischi fisici vengono combinati in un array per una velocità e/o una resistenza ai guasti migliorate.


**RAID 0** (Stripe Set senza parità/Array non ridondante) implementa lo striping di dati in cui i blocchi di file vengono scritti su più unità in frammenti e richiede un minimo di due dischi. Il vantaggio di un RAID 0 è che la velocità di lettura/scrittura è aumentata notevolmente. Più sono i dischi nell'array e maggiore è la larghezza di banda. Lo svantaggio di un RAID0 è che non c'è alcuna tolleranza ai guasti. Di conseguenza, il malfunzionamento di una singola unità distrugge l'array. Inoltre, un RAID 0 non implementa il controllo degli errori. Pertanto, qualsiasi errore è anche irreversibile. Una soluzione comune per la tolleranza ai guasti consiste nel disporre di un'unità esterna all'array che viene utilizzata come archiviazione di backup in caso di malfunzionamento hardware.

**RAID 1** (Mirrored set senza parità) implementa il mirroring di dati. I dati vengono duplicati su 2 o 4 unità tramite un controller raid hardware, fornendo così un certo grado di tolleranza ai guasti. L'array è recuperabile se almeno un'unità non è malfunzionante. Fornisce prestazioni di lettura più rapide di una singola unità e fornisce la ridondanza di unità se si verifica un malfunzionamento di unità. C'è anche una leggera riduzione della velocità di scrittura.

**RAID 5** (Stripe Set con parità distribuita duale) Implementa lo striping di dati a un livello di blocco e distribuisce la parità tra le unità. Le informazioni di parità consentono il ripristino dall'errore di qualsiasi singola unità perché le eventuali letture successive possono essere calcolate dalla parità distribuita. Raid 5 consente anche delle velocità di lettura/scrittura aumentate e consente l'uso più efficiente dello spazio su disco. RAID 5 richiede un minimo di tre dischi.

**RAID 10** (RAID 1 + 0) Crea più mirror, dove i dati vengono organizzati come stripe su più dischi e quindi viene eseguito il mirroring dei set di dischi in striping. RAID 10 offre la stessa tolleranza ai guasti di RAID 1 con velocità di lettura/scrittura aumentate rispetto a una singola unità o un singolo volume Raid 1. RAID livello 10 richiede quattro unità per l'implementazione.

