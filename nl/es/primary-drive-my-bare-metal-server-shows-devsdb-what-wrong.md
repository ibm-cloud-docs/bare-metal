---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# La unidad primaria en mi servidor nativo aparece como /dev/sdb. ¿Qué ocurre?

Puede deberse a que el disco virtual de IPMI ocupe la ranura /dev/sda. Se puede inhabilitar de forma segura conectándose a IPMIView y navegando al separador de soporte virtual. Seleccione **Opciones > Inhabilitar** y pulse el botón **Aplicar** para realizar el cambio. La próxima vez que se reinicie el servidor nativo, la unidad primaria se mostrará como /dev/sda.
