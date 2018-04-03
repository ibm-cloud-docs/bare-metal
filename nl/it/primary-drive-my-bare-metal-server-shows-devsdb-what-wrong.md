---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# L'unità primaria sul mio server bare metal si presenta come /dev/sdb. Cos'è che non va?

La causa potrebbe essere il disco virtuale di IPMI che prende lo slot /dev/sda. È possibile eseguirne senza alcun rischio la disabilitazione stabilendo una connessione a IPMIView e accedendo alla scheda Virtual Media. Seleziona **Options > Disable** e fai clic sul pulsante **Apply** per apportare la modifica. Al successivo riavvio del server bare metal, l'unità primaria visualizzerà /dev/sda.
