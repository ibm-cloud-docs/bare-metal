---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: bare metal, spare pools

subcollection: bare-metal

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

Il pool di riserva è una forma di messa in pausa di alcuni dispositivi designati come riserve che hanno la capacità di subentrare al flusso di lavoro di un dispositivo primario o agire come un nuovo dispositivo nel parco dispositivi del cliente. In modo che un dispositivo venga designato come riserva, deve essere aggiunto al pool di riserva e associato a un dispositivo primario. Attieniti alla seguente procedura per aggiungere un dispositivo al pool di riserva.
{:shortdesc}

1. Accedi alla [console {{site.data.keyword.cloud}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/){: new_window} utilizzando le tue credenziali univoche.
2. Seleziona **Devices > Spare Pool** dalla barra di navigazione per accedere alla schermata *Spare Pool*.
3. Fai clic sul link **Add to Spare Pool**.

   Sarà popolato un elenco di dispositivi idonei per l'aggiunta al pool di riserva.
   {:tip}

4. Seleziona i dispositivi da aggiungere al pool di riserva. 
5. Fai clic su **Add Selected Devices**.
6. Fai clic su **Confirm** per aggiungere i dispositivi al pool di riserva.

## Passi successivi
Dopo aver avviato un trasferimento del dispositivo al pool di riserva, il dispositivo viene passato al pool di riserva entro un'ora. Dopo che il dispositivo diventa attivo nel pool di riserva, viene visualizzato nella schermata Spare Pool e può essere designato come un hot spare per un dispositivo primario.
