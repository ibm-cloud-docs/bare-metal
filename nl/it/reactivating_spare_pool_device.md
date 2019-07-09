---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

keywords: bare metal reactivate spare pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Riattivazione di un dispositivo dal pool di riserva
{: #bm-reactivating-spare-pools}

Quando un dispositivo viene aggiunto al pool di riserva, il suo stato all'interno dell'elenco dei dispositivi viene modificato da attivo (Active), che indica che il dispositivo è idoneo per le interazioni standard, a pool di riserva (Spare Pool). I dispositivi che fanno parte del pool di riserva sono dedicati a tale funzione e non possono essere utilizzati per le normali azioni giornaliere come gli altri dispositivi. Per rimuovere un dispositivo dal pool di riserva in modo che possa ritornare alla sua funzione tradizionale, è necessario riattivarlo.
{:shortdesc}

## Riattivazione di un dispositivo dal pool di riserva

1. Accedi a [{{site.data.keyword.cloud}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/){: new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Devices > Spare Pool** dalla barra di navigazione per accedere alla schermata *Spare Pool*.
3. Seleziona **Actions > Reactivate Device** per il dispositivo desiderato.
4. Fai clic su **Yes** per riattivare il server. Fai clic su **No** per annullare l'azione.

## Passi successivi
Dopo aver avviato il processo di riattivazione, il dispositivo viene portato offline, il firmware viene aggiornato e il dispositivo diventa disponibile per l'utilizzo regolare. Il processo di riattivazione impiega circa un'ora. I dispositivi che vengono rimossi dal pool di riserva non sono più idonei per l'utilizzo come metodo di failover. Il dispositivo può ritornare nel pool di riserva in qualsiasi momento aggiungendolo nuovamente al pool di riserva. Per ulteriori informazioni, vedi [Aggiunta di un dispositivo al pool di riserva](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools).
