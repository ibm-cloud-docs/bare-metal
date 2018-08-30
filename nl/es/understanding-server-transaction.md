---
copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Transacciones de servidor

Cuando se suministra un servidor en {{site.data.keyword.Bluemix_short}}, se carga un sistema operativo o se instala un software, se coloca en una *transacción*.  Una transacción es una serie de pasos automatizados realizados por los sistemas de gestión de {{site.data.keyword.Bluemix_notm}} para configurar servidores de clientes.

Si uno de los servidores está en una transacción, aparece un enlace en las notas del servidor en los listados de hardware.  Puede pulsar este enlace para ver qué transacciones están pendientes para ese servidor específico.  Aparece una tabla que lista los datos de la transacción actual que está en curso.

* **ID** es el ID interno de la transacción.  Si envía una incidencia sobre una transacción, incluya este número.
* **Grupo** es una breve descripción del tipo de transacción.  Por ejemplo, *MS OS Reload* significa que se está recargando un sistema operativo Microsoft en la máquina.
* **Estado actual** es el nombre del paso actual de la transacción.  Por ejemplo, *INSTALL_OS* es un paso de transacción de *MS OS Reload* que significa que actualmente se está instalado Windows en la máquina.
* **Tiempo transcurrido y Tiempo promedio** trabajan conjuntamente.  Tiempo transcurrido muestra durante cuánto tiempo se ha ejecutado el paso actual de la transacción.  Tiempo promedio muestra la cantidad de tiempo que suele tardar, de media, este paso.  Si el tiempo transcurrido es significativamente mayor que el tiempo promedio, es posible que desee abrir una incidencia de soporte sobre el estado.
