---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Nome e ubicazione del daemon di monitoraggio RAID
{{site.data.keyword.cloud}} utilizza soprattutto schede RAID LSI e Adaptec con alcune eccezioni per l'hardware legacy. La seguente tabella mostra le ubicazioni del gestore RAID, le ubicazioni del monitoraggio, le configurazioni e le impostazioni degli avvisi RAID.

Puoi configurare gli avvisi RAID per tralasciare il processo di monitoraggio del portale modificando il server SMTP e la destinazione della email di notifica nella configurazione per una scheda RAID. Se modifichi queste configurazioni, IBM non può informarti dei problemi RAID o tenere automaticamente traccia del problema fino alla sua risoluzione. Non modificare la configurazione fornita a meno che tu non sia consapevole dei rischi.

<caption>Tabella 1. Configurazioni e impostazioni RAID</caption>

||Linux LSI|Windows LSI|Linux Adaptec|Windows Adaptec|
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
|**Opzioni di notifica alternative**|Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiede le appropriate configurazioni del firewall.|Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiede le appropriate configurazioni del firewall.|Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiede le appropriate configurazioni del firewall.|Modifica il server SMTP in un server SMTP locale. Il server SMTP locale richiede le appropriate configurazioni del firewall.|
