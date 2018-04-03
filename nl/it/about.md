---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introduzione a {{site.data.keyword.baremetal_short}}

I {{site.data.keyword.baremetal_long}} ti offrono prestazioni e controllo. I {{site.data.keyword.baremetal_short}} non vengono eseguiti in un hypervisor e ottieni un accesso di basso livello alle risorse hardware. Inoltre, non condividerai il server con altri clienti; è tutto tuo!
{:shortdesc}

Quando crei un {{site.data.keyword.baremetal_short}}, puoi personalizzare le specifiche, da processori e regione a sistema operativo e disco rigido.

Per eseguire il provisioning di un {{site.data.keyword.baremetal_short}}:
  1. Vai a **Calcola > {{site.data.keyword.baremetal_short}}** e fai clic su **Aggiungi**.
  2. Seleziona l'ubicazione nella quale desideri che venga eseguito il provisioning dell'istanza {{site.data.keyword.baremetal_short}}. Questo è un data center in una delle regioni {{site.data.keyword.Bluemix}}.
  3. Seleziona la configurazione per i server. Questa configurazione si applica a tutti i server creati per questa istanza.
  4. Seleziona il numero di server che desideri venga creato per questa istanza Per ciascun server, immetti un nome host univoco.
  5. **Facoltativo** immetti un URL a uno script o a un file di testo da te definito per configurare il server. Lo script di provisioning deve utilizzare un protocollo HTTPS. Lo script verrà scaricato ed eseguito dopo l'esecuzione del provisioning dell'istanza, se possibile. Se l'URL non è associato a uno script eseguibile, lo script verrà semplicemente scaricato.
  6. Seleziona il sistema operativo per i server. Questo sistema operativo si applica a tutti i server creati per questa istanza.

Entro un'ora, verrà eseguito il provisioning del tuo {{site.data.keyword.baremetal_short}} che sarà quindi disponibile per l'uso.
