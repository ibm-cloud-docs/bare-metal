---

copyright:
  years: 1994, 2019
lastupdated: "2018-07-10"

keywords: raid controller commands, raid commands

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Comandi del controller RAID
{: #bm-raid-controller-commands}

Per eseguire i comandi del controller RAID, utilizza il programma di utilità della riga di comando Adapatec.
Di seguito sono riportati i comandi del controller RAID più comuni che potresti utilizzare.
{:shortdesc}

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ elenca il tipo di operazione, il numero di unità logica, la dimensione
dell'unità logica e l'avanzamento dell'operazione. Puoi anche vedere lo stato di qualsiasi comando in esecuzione in background, ad esempio i seguenti elementi:
<ul>
  <li> Ricostruzione più recente
  <li> Sincronizzazione
  <li> Migrazione unità logica
  <li> Compressione/espansione
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ elenca le informazioni su controller, unità logiche e unità fisiche. Puoi vedere informazioni come i seguenti elementi:
<ul>
  <li> Tipo di controller
  <li> BIOS, blocco di avvio, driver dell'unità e versioni del firmware
  <li> Tipo di dispositivo fisico, ID dispositivo, presenza di PFA
  <li> Stato del dispositivo fisico
  <li> Informazioni sulla custodia: ventola, alimentazione e temperatura
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ ti fornisce l'accesso ai log di stato e di evento di un controller. _DEVICE xxx_ visualizza un log di tutti gli errori del dispositivo rilevati dal controller.

Vedi il seguente esempio relativo all'output che viene generato utilizzando il comando _GETLOGS_:
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
Utilizzi questo comando per mostrare le unità specifiche e tutti i possibili errori di unità che potrebbe avere. 
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
Questo comando visualizza lo stato di ricostruzione di tutte le unità e il tempo stimato per completare la ricostruzione. Quando esegui il comando, visualizzi questo output:
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
con questo: 
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
**Nota:** rimuovi la tag "do-email" per il livello "WARNING". In alternativa, modifica il livello di sicurezza in "INFO".

## Errori comuni dell'unità
{: #bm-common-drive-errors}

Gli errori driver più comuni sono gli errori smart, gli errori hardware e gli errori del supporto. Questi errori vengono visualizzati se un'unità sta smettendo di funzionare. Quindi, devi sostituire l'unità il prima possibile.

Sebbene non insoliti, i comandi interrotti sono un altro errore comune. Tuttavia, se i comandi interrotti aumentano di numero (come 100), apri un ticket di supporto.  

Gli errori di collegamento possono indicare che potrebbe essere necessario riposizionare o sostituire un cavo.

### Informazioni sui ticket di supporto
{: #bm-raid-support}

**Schede RAID Adaptec** <br>
Quando crei un ticket di supporto, assicurati di includere l'output completo di `arcconf getconfig 1/arcconf getlogs 1 device tabular`. Fornendo queste informazioni aiuti il team di supporto a identificare l'ordine di unità, l'appartenenza dell'array, la geometria dell'array e i problemi di cablaggio. Queste informazioni sono fondamentali per il ripristino di una configurazione RAID che è andata persa. Concedere l'autorizzazione di riavvio/spegnimento nell'aggiornamento iniziale o chiederne la sostituzione a sistema acceso aiuta ad accelerare il processo per il ticket di supporto. 

**Schede RAID LSI** <br>
Utilizza i seguenti comandi per ottenere i file di log per le schede RAID LSI. Devi includere l'output completo di questi file di log nel tuo ticket di supporto.
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Nota**: assicurati di eseguire il backup di qualsiasi lavoro prima di effettuare la risoluzione dei problemi.
