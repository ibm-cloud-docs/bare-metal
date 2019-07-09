---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Informazioni sui ticket di supporto RAID
{:# bm-raid-support-ticket}

Se hai un problema o una domanda sull'utilizzo di RAID sul tuo server bare metal, potresti trovare una risposta nel forum [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window}.
Puoi anche aprire un ticket di supporto. Per informazioni sui ticket di supporto, vedi [Apertura di un ticket di supporto.](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> Quando apri un ticket di supporto, devi fornire i file di log RAID. Le informazioni contenute nei file di log RAID sono fondamentali per il ripristino di una configurazione RAID che è andata persa. Fornendo i tuoi file di log aiuti il team di supporto a identificare l'ordine di unità, l'appartenenza dell'array, la geometria dell'array e i problemi di cablaggio. A seconda del tipo di controller RAID che stai utilizzando, Adaptec o LSI, utilizza i seguenti comandi per ottenere i file di log RAID.

**Nota:** concedere l'autorizzazione di riavvio/spegnimento nell'aggiornamento iniziale o chiedere che l'unità venga sostituita a sistema acceso aiuta ad accelerare il processo per il ticket di supporto. 

<b>Schede RAID Adaptec</b><br>
Utilizza il seguente comando per ottenere i file di log per le schede RAID Adaptec. Assicurati di includere l'output completo di questo file di log nel tuo ticket di supporto.

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>Schede RAID LSI</b><br>
Utilizza i seguenti comandi per ottenere i file di log per le schede RAID LSI. Devi includere l'output completo di questi file di log nel tuo ticket di supporto.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**Importante:** assicurati di eseguire il backup di qualsiasi lavoro prima che inizi la risoluzione dei problemi.
