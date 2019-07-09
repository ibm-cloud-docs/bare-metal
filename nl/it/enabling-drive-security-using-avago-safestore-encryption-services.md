---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Abilitazione della protezione dell'unità utilizzando i servizi di crittografia Avago SafeStore
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

La configurazione della protezione dell'unità aiuta ad evitare l'accesso ai dati archiviati su dischi rimossi senza una chiave di sicurezza. I dati dell'unità non possono essere recuperati senza questa chiave. {{site.data.keyword.BluSoftlayer_full}} fornisce SED (Self-Encrypting Drives) in data center selezionati per unità che possono essere acquistate su un server bare metal. Sono disponibili delle unità SATA da 10 TB nei nostri data center US.

## Prerequisiti 
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* Server bare metal con unità SED - SATA 10 TB
* LSI/AVAGO MegaRAID SAS 9361 -8i o schede RAID LSI/AVAGO simili
* Software Mega RAID Storage Manager installato

## Abilitazione della protezione dell'unità utilizzando MSM (MegaRAID Storage Manager)
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

L'utente può impostare la chiave di sicurezza e proteggere i dati in un disco rimosso utilizzando MSM (MegaRAID Storage Manager). Puoi anche utilizzare l'interfaccia WebBIOS che richiede una chiave di sicurezza all'avvio del server per immettere il BIOS della scheda MegaRAID per configurare l'impostazione della protezione dell'unità. Per ulteriori informazioni su MegaRAID Controller Card SAS 9361-8i, vedi il sito Broadcom, [MegaRAID SAS 9361-8i ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation).

### Identificazione delle unità SED preinstallate
{: #identifying-preinstalled-sed-drives}

MSM (MegaRAID Storage Manager) viene fornito preinstallato sulla maggior parte dei sistemi operativi supportati. Se non è presente, puoi installarlo manualmente dal sito Broadcom. Per ulteriori informazioni, vedi [MegaRAID SAS 9361-8i downloads](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads).

Puoi aprire MSM (MegaRAID Storage Manager) utilizzando le credenziali di sistema. Nell'esempio, viene utilizzato un ambiente Windows e MSM è preinstallato.

Quando avvii MSM, devi immettere nome utente (**User name**) e **Password** ossia l'utente privilegiato (amministratore) e la password.

Fai clic sulla scheda **Physical** e sulle unità disponibili sul sistema. Nel pannello **Properties** è presente la sezione
**Drive Security Properties** che include il campo **Full Disk Encryption capable**, che mostra **Yes**. Nell'esempio utilizzato, vengono utilizzati due dischi non SED e quattro dischi SED.

### Abilitazione della protezione dell'unità sul controller
{: #enabling-drive-security-at-the-controller}

1. Per abilitare la protezione dell'unità, fai clic con il tasto destro su **Controller 0 :AVAGO MegaRAID SAS 9361-8i** dalla scheda **Physical** e seleziona
**Enable Drive Security**.
  * Puoi ora immettere l'identificativo della chiave di sicurezza (**Security key identifier**) e la chiave di sicurezza (**Security key**). Se disponi di più chiavi di sicurezza, un identificativo della chiave di sicurezza può aiutarti ad identificare quale chiave di sicurezza devi utilizzare. Devi registrare la chiave di sicurezza in un'ubicazione sicura. La chiave di sicurezza è obbligatoria quando riconfiguri le unità ad esempio rimuovendo o reimmettendo un'unità. Senza la chiave di sicurezza, non è possibile richiamare i dati archiviati in un volume creato all'esterno delle SED. Non è possibile richiamare una chiave di sicurezza dimenticata. Può anche essere impostata una password di avvio, che mette in pausa il sistema in attesa che venga inserita la password qui impostata. La password di avvio è facoltativa e se impostata devi accedere a IPMI ed immettere la password di avvio se il sistema viene riavviato. Scorri verso il basso e seleziona la casella che indica **I recorded the security settings for future reference** e fai clic su **Yes** per abilitare la protezione dell'unità.
  * Quando la protezione dell'unità è abilitata, viene visualizzata un'immagine di una chiave gialla per **Controller 0 AVAGO MegaRAID SAS 9361-8i**.
2. Ora crea un volume sicuro utilizzando le SED. Fai clic con il tasto destro su **Controller0** dalla scheda **Logical** e seleziona  
**Create Virtual Drive**.
3. Scegli l'opzione **Advanced**. La schermata deve specificare **RAID level** e **Drive security method** per
**Full Disk encryption (FDE)**. Seleziona le unità FDE necessarie e fai clic su **Add** > **Create Drive Group** > **Next**.
4. Controlla le impostazioni dell'unità virtuale e apporta tutte le modifiche necessarie. L'impostazione suggerita per **Read Policy** è **Always Read Ahead**. L'impostazione suggerita per **Write policy** è **Write Back**. Fai clic su **Create Virtual Drive**. Accetta l'impatto della politica Write Back dovuto a BBU facendo clic su **Yes**. Fai clic su **Next** e controlla la schermata di riepilogo. Fai clic su **Finish**.
5. Per confermare che il disco virtuale sia protetto, fai clic sulla scheda **Logical** e sull'unità virtuale che è stata creata. Vedi in **Drive Security Properties** che il campo **Secured** è contrassegnato con **Yes**.

Se il server viene fornito con dei volumi RAID che sono già stati creati utilizzando le unità SED, puoi rendere il volume sicuro seguendo questa procedura.

Nella scheda **Logical**, fai clic con il tasto destro su **Drive Group** e seleziona **Secure Using FDE**. Se ha in un misto di unità FED e non FED
per un volume, questa opzione non è visibile.

Per rimuovere la protezione dell'unità, devi prima eliminare i dischi virtuali protetti e fare clic con il tasto destro su Controller 0 per **Disable Drive Security**. Questa funzione cancella in modo sicuro i dati contenuti e rimuove la protezione dell'unità.

Puoi anche configurare la protezione dell'unità utilizzando webBIOS e accedendo tramite IPMI all'avvio e immettendo il BIOS RAID. <!--For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.-->
