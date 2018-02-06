---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Das primäre Laufwerk auf dem Bare-Metal-Server wird als "/dev/sdb" angezeigt. Was ist falsch?

Dies kann daran liegen, dass die virtuelle IPMI-Platte den "/dev/sda"-Slot belegt. Dies kann sicher inaktiviert werden, in dem Sie eine Verbindung zu IPMIView herstellen und zur Registerkarte "Virtueller Datenträger" navigieren. Wählen Sie **Optionen > Inaktivieren** aus und klicken Sie auf die Schaltfläche **Anwenden**, um die Änderung zu übernehmen. Wenn der Bare-Metal-Server neu gebootet wird, wird für das primäre Laufwerk "/dev/sda" angezeigt.
