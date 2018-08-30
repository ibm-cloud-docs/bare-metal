---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Annullamento dei pool di riserva 
{: #adding-spare-pools}

I dispositivi aggiunti al pool di riserva possono essere annullati solo dalla schermata Spare Pool all'interno del{{site.data.keyword.slportal_full}}. L'annullamento di un dispositivo nel pool di riserva è identico a quello di un dispositivo all'interno dell'elenco dei dispositivi (Device List).Completa la seguente procedura per annullare un dispositivo nel pool di riserva.
{:shortdesc}

## Annullamento dei pool di riserva

1. Esegui il backup di tutti i dati che desideri conservare dal dispositivo di cui è in corso l'annullamento.

   L'annullamento di un dispositivo comporta la rimozione di tutti i dati dal dispositivo annullato. Tutte le informazioni memorizzate nel dispositivo non possono essere richiamate dopo che il dispositivo è stato annullato.
   {:tip}

2. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
3. Seleziona **Devices > Spare Pool** dalla barra di navigazione per accedere alla schermata *Spare Pool*.
4. Seleziona **Actions > Cancel Device** per lo specifico dispositivo.
5. Seleziona il motivo dell'annullamento dall'elenco a discesa **Reason**.
6. Immetti un breve spiegazione dell'annullamento nella casella di testo fornita.
7. Fai clic su **Continue** per procedere alla schermata successiva. Fai clic su **Cancel** per arrestare il processo di annullamento e ritornare alla schermata Spare Pool.
8. Seleziona **Data Loss Acknowledgement** per riconoscere che può verificarsi una perdita di dati come parte del processo di annullamento.
9. Fai clic su **Cancel Device** per annullare il dispositivo. Fai clic su **Close** per arrestare il processo di annullamento e ritornare alla schermata Spare Pool.

## Passi successivi
Dopo aver richiesto l'annullamento di un dispositivo nel pool di riserva, il dispositivo viene pianificato per l'annullamento. Il dispositivo viene immediatamente recuperato e rimosso dall'account.
