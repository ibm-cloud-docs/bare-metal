---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Iniciación a los {{site.data.keyword.baremetal_short}}

Los {{site.data.keyword.baremetal_long}} proporcionan rendimiento y control. Los {{site.data.keyword.baremetal_short}} no se ejecutan en un hipervisor, y el usuario obtiene acceso de bajo nivel a los recursos de hardware. Además, el servidor no se comparte con otros clientes, ¡es todo suyo!
{:shortdesc}

Al crear un dispositivo de {{site.data.keyword.baremetal_short}}, puede personalizar las especificaciones, desde los procesadores y la región hasta el sistema operativo y el disco duro.

Para suministrar un dispositivo de {{site.data.keyword.baremetal_short}}:
  1. Vaya a **Calcular > {{site.data.keyword.baremetal_short}}** y pulse **Añadir**.
  2. Seleccione la ubicación en la que desea que se suministre la instancia de {{site.data.keyword.baremetal_short}}. Se trata de un centro de datos en una de las regiones de {{site.data.keyword.Bluemix}}.
  3. Seleccione la configuración de los servidores. Esta configuración se aplica a todos los servidores creados para esta instancia.
  4. Seleccione el número de servidores que ha creado para esta instancia. Para cada servidor, especifique un nombre de host exclusivo.
  5. **Opcional:** especifique un URL a un script o archivo de texto que haya definido para configurar el servidor. El script de suministro debe utilizar un protocolo HTTPS. El script se descargará y se ejecutará después de que se haya suministrado la instancia, si es posible. Si el URL no está asociado a un script ejecutable, el script sólo se descargará.
  6. Seleccione el sistema operativo de los servidores. Este sistema operativo se aplica a todos los servidores creados para esta instancia.

Pasada una hora, se habrá suministrado el dispositivo de {{site.data.keyword.baremetal_short}} y estará disponible para utilizarse.
