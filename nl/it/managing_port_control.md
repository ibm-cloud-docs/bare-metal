---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gestione del controllo porta per un dispositivo
{: #bm-manage-port-control}

Ogni dispositivo associato a un account dispone di due porte di rete che ricevono il traffico in entrata, una per il traffico di rete pubblica e una per il traffico di rete privata. Puoi abilitare o disabilitare queste porte in qualsiasi momento per controllare il traffico di rete ricevuto da un dispositivo. Completa la seguente procedura per aggiornare le impostazioni di controllo porta per un dispositivo.

## Prima di iniziare
* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Assicurati di disporre di tutte le autorizzazioni di account necessarie e dell'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione di **Gestione utenti** dell'infrastruttura classica può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione dell'accesso al dispositivo](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Gestisci il controllo porta per un dispositivo

1. Accedi all'**Elenco dispositivi** e seleziona il **Nome dispositivo** da aggiornare.  
2. Fai clic sull'elenco a discesa **Azioni** per il dispositivo.
3. Seleziona **Controllo porta**.
4. Aggiorna le caselle a discesa *Rete pubblica* e/o *Rete privata* completando una delle seguenti azioni:
   * Seleziona la velocità desiderata per abilitare l'accesso di rete.
   * Seleziona Disconnesso per disabilitare l'accesso di rete.
5. Fai clic sul pulsante Aggiorna.
6. Fai clic sul pulsante Chiudi per chiudere la finestra.

## Passi successivi

Se hai selezionato **Disabilitato**, l'accesso di rete per la porta disabilitata cessa per l'interfaccia del dispositivo. Se hai selezionato **Abilitato**, l'accesso di rete è disponibile per la porta abilitata. Il controllo porta rimane nell'impostazione selezionata finché non viene modificato manualmente.
