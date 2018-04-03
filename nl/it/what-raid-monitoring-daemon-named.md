---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Nome e ubicazione del daemon di monitoraggio RAID
{{site.data.keyword.cloud}}, utilizzo soprattutto schede RAID LSI e Adaptec con alcune eccezioni per l'hardware legacy. Il grafico di seguito mostra le ubicazioni del gestore RAID, le ubicazioni del monitoraggio, le configurazioni e le impostazioni degli avvisi RAID.

Puoi configurare gli avvisi RAID per tralasciare il processo di monitoraggio del portale modificando il server SMTP e la destinazione della email di notifica nella configurazione per una specifica scheda RAID. Quando queste configurazioni vengono modificate, IBM non puoi informarti dei problemi RAID o tenere automaticamente traccia del problema fino alla sua risoluzione. Non modificare la configurazione fornita a meno che tu non sia consapevole dei rischi.

||LSI - Linux|LSI - Windows|Adaptec - Linux|Adaptec - Windows|
|---|---|---|---|---|
|**Nome gestore**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Ubicazione gestore**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nome monitoraggio**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Ubicazione monitoraggio**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nome processo**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Ubicazione log**|Ubicazione dei log di messaggi predefinita per il sistema operativo, ad es. /var/log/messages|Solo GUI|/usr/StorMan/RaidEvtA.log|Solo GUI|
|**Destinazione email di notifica**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Formato di origine email di notifica**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**Porta email**|25|25|25|25|
|**Server SMTP**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Opzioni di notifica alternative**|Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiederà le appropriate configurazioni del firewall. |Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiederà le appropriate configurazioni del firewall. |Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiederà le appropriate configurazioni del firewall. |Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiederà le appropriate configurazioni del firewall. |
