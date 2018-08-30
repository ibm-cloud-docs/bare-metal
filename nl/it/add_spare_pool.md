---



copyright:
  years: 2014, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Aggiunta di pool di riserva 
{: #adding-spare-pools}

Il pool di riserva è una forma di failover dove alcuni dispositivi sono designati come hot spare e possono assumersi il flusso di lavoro di un dispositivo primario se quest'ultimo ha un malfunzionamento. Un dispositivo, per essere designato come hot spare, deve essere aggiunto al pool di riserva e associato a un dispositivo primario. Completa la seguente procedura per aggiungere un dispositivo al pool di riserva:
{:shortdesc}

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Devices > Spare Pool** dalla barra di navigazione per accedere alla schermata *Spare Pool*.
3. Fai clic sul link **Add to Spare Pool**.
   
   Sarà popolato un elenco di dispositivi idonei per l'aggiunta al pool di riserva.
   {:tip}
   
4. Seleziona i dispositivo da aggiungere al pool di riserva.
5. Fai clic su **Add Selected Devices**.
6. Fai clic su **Confirm** per aggiungere i dispositivi al pool di riserva. 

## Passi successivi
Dopo aver avviato un trasferimento del dispositivo al pool di riserva, il dispositivo viene passato al pool di riserva entro un'ora. Dopo che il dispositivo diventa attivo nel pool di riserva, viene visualizzato nella schermata Spare Pool e può essere designato come un hot spare per un dispositivo primario.
