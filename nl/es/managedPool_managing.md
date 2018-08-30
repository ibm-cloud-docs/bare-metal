---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---

# Especificación del número de servidores de la agrupación gestionada por el cliente

Establezca el número de servidores de la agrupación gestionada utilizando la siguiente llamada de API:

|Llamada de API|Parámetros|Descripción|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">Establecer cantidad de agrupación gestionada</a>|poolKeyName|Nombre de clave que identifica la agrupación. IBM le proporciona este valor.|
|  | backendRouter | Identifica el direccionador de fondo de la agrupación. IBM le proporciona este valor.|
|  | cantidad | El número total de servidores que desea en la agrupación.<br><br>Si el número actual de servidores de la agrupación es menor que el valor que proporciona aquí, se añadirán los servidores.<br>Si el número actual de servidores de la agrupación es superior al valor que proporciona aquí, los servidores se eliminan.|
