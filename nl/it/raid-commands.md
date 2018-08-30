---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Comandi controller RAID

Utilizzi l'utilità riga di comando Adaptec per eseguire i comandi controller RAID.
Di seguito sono riportati i comandi controller RAID più comuni che potresti utilizzare.
{:shortdesc}

**Nota:** Windows e VMware hanno percorsi differenti per eseguire i comandi storcli. Vedi i seguenti esempi per il corretto percorso del comando.

Windows (utilizza CMD)
`C:\Program Files (x86)\MegaRAID Storage Manager>`      
oppure
`C:\Program Files\LSIStorCli>`

VMware (devi installare storcli prima di eseguire i comandi storcli)
`/opt/lsi/storcli/`

## Comandi controller RAID comuni

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ elenca il tipo di operazione, il numero di unità logica, la dimensione di unità logica e l'avanzamento dell'operazione. Puoi anche vedere lo stato degli eventuali comandi in background in esecuzione, come ad esempio i seguenti elementi:
<ul>
  <li> Ricompilazione più recente
  <li> Sincronizzazione
  <li> Migrazione di unità logica
  <li> Compattazione/espansione
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ elenca le informazioni su controller, unità logiche e unità fisiche. Puoi vedere informazioni quali i seguenti elementi:
<ul>
  <li> Tipo di controller
  <li> BIOS, blocco di avvio, driver di dispositivo e versioni firmware 
  <li> Tipo di dispositivo fisico, ID dispositivo, presenza di PFA 
  <li> Stato dell'unità fisica 
  <li> Informazioni sull'enclosure: ventola, alimentatore e temperatura
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ ti fornisce l'accesso ai log di stato ed evento di un controller. _DEVICE xxx_ visualizza un log degli eventuali errori dispositivo riscontrati dal controller.

Vedi il seguente esempio per l'output generato utilizzando il comando _GETLOGS_:
```
driveErrorEntry
smartError.. ............................ false 
vendorID ................................ WDC
serialNumber ............................ WD-XXX
wwn ..................................... xxxxxxxxxxxxxxxx - CC_FILTER
deviceID ................................ 10
productID ............................... WD1003FB
numParityErrors ......................... 0
linkFailures ............................ 0
hwErrors ................................ 0
abortedCmds ............................. 7
mediumErrors ............................ 20
smartWarning ............................ 0
```

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir” </code></b><br>
Utilizzi questo comando per visualizzare le specifiche unità e gli eventuali errori unità possibili che potrebbe presentare  
Il seguente esempio mostra l'output:
```
Drive /c0/e252/s0 - Detailed Information: 
Shield Counter = 0
 Media Error Count = 0
 Other Error Count = 0 
Drive Temperature = 24C (75.20 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = XXXX 
Firmware Revision = SN04

 Drive /c0/e252/s1 - Detailed Information: 
Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 22C (71.60 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = xxxx 
Firmware Revision = SN03 

Drive /c0/e252/s2 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 21C (69.80 F)
 Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No
 SN = xxxx 
Firmware Revision = SN04

 Drive /c0/e252/s3 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0
 Other Error Count =
 Drive Temperature = 23C (73.40 F) 
Predictive Failure Count = 0
 S.M.A.R.T alert flagged by drive = No 
SN = xxxx
Firmware Revision = SN03  
```

<!--<code><b>/opt/MegaRAID/storcli/storcli64 /c0 show all | less </code></b>-->
<!--You use this command to view RAID health, size, name, and other important information.-->

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild</code></b>
Questo comando visualizza lo stato della ricompilazione di tutte le unità e il tempo stimato di completamento della ricompilazione. Puoi vedere questo output quando esegui il comando:
```
---------------------------------------------
Drive-ID Progress% Status Estimated Time Left 
---------------------------------------------
/c0/e252/s0 - Not in progress
 /c0/e252/s1 - Not in progress
 /c0/e252/s2 - Not in progress
 /c0/e252/s3 - Not in progress
--------------------------------------------- 
```

<b>RAID alert "Spam"</b>
Modifica la sezione "global" della configurazione predefinita (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml): 
```<global>
 <severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity>
<severity level="CRITICAL"> 
<do-email/>
 <do-systemlog/> 
</severity>
 <severity level="WARNING">
 <do-email/> 
<do-systemlog/> 
</severity>
 <severity level="INFO"> <do-systemlog/>
</severity>
 </global> 
```
to this: 
```
<global> 
<severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity> 
<severity level="CRITICAL"> 
<do-email/> 
<do-systemlog/> 
</severity> 
<severity level="WARNING"> 
<do-systemlog/> 
</severity> 
<severity level="INFO">
<do-systemlog/>
 </severity> 
</global> 
```
**Nota:** rimuovi la tag "do-email" per il livello "WARNING". In alternativa, modifica il livello di sicurezza in "INFO"

## Errori unità comuni

Gli errori unità più comuni sono gli errori smart, gli errori hardware e gli errori supporto. Vedi questi errori se si sta verificando un malfunzionamento di un'unità. Devi quindi sostituire l'unità quanto prima possibile.

Anche se non comuni, i comandi interrotti sono un altro errore comune. Se però i comandi interrotti aumentano di numero (come ad esempio 100), apri un ticket di supporto.  

Gli errori di collegamento possono indicare che potrebbe essere necessario riposizionare o sostituire un cavo.

## Informazioni sui ticket di supporto

<b>Schede RAID Adaptec</b>
Assicurati di includere l'output completo di `arcconf getconfig 1/arcconf getlogs 1 device tabular` quando crei un ticket di supporto. Fornire queste informazioni aiuta il team di supporto a identificare l'ordine di unità, l'appartenenza all'array, la geometria dell'array e i problemi di cablaggio. Queste informazioni sono critiche per il ripristino di una configurazione RAID perduta. Concedere l'autorizzazione a riavviare/spegnere nell'aggiornamento iniziale o richiedere che ne venga eseguito l'hot swap accelera il processo del ticket di supporto. 

<b>Schede RAID LSI</b>
Utilizzare i seguenti comandi per ottenere i file di log per le schede RAID LSI. Devi includere l'output completo di questi file di log con il tuo ticket di supporto.
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Nota**: assicurati di eseguire il backup dell'eventuale lavoro prima che venga eseguita la risoluzione dei problemi.
