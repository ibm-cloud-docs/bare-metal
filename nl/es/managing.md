---



copyright:

  years: 2016
lastupdated: "2016-01-19"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Gestión de servidores nativos
{: #managing}


Puede detener, iniciar, reiniciar y cancelar servidores.
{:shortdesc}

## Réplica de una instancia de servidor
Puede copiar o clonar una instancia de servidor nativo para replicar la configuración del servidor y poner un nuevo servidor en funcionamiento rápidamente.
{:shortdesc}

Para clonar la instancia:
 1. Vaya al menú y seleccione **Configurar réplica**. Se copiarán todas las configuraciones. No se copiarán los datos ni el contenido.
 2. Especifique un nombre de servidor exclusivo.
 3. Especifique el nombre de dominio.

## Recarga del sistema operativo
De vez en cuando, quizá desee recargar el sistema operativo en el servidor.
{:shortdesc}

Para recargar el sistema operativo:
 1. Realice una copia de seguridad de todos los datos antes de empezar. Si omite este paso, se perderán todos los datos existentes y no se podrán recuperar.
 2. Vaya al menú y seleccione **Recarga de SO**. Puede seleccionar:
  * Cambiar el sistema operativo a uno distinto y volver a empezar con configuraciones nuevas.
  * Mantener el sistema operativo existente con las configuraciones actuales, pero borrar el servidor para empezar de nuevo.

Durante la recarga de SO, el servidor estará fuera de línea y no se podrá utilizar. El tiempo de recarga varía en función de la capacidad del servidor y el sistema operativo. Si ha definido un script de suministro, todas las configuraciones se restaurarán al finalizar la recarga. Si ha realizado una copia de seguridad de los datos antes de la recarga de SO, puede cargarlos en el servidor cuando esté disponible.

## Supresión de la instancia de servidor
Si ya no necesita la instancia de servidor del servidor nativo y no desea pagar por ella, puede suprimirla en cualquier momento.
{:shortdesc}

Para suprimir la instancia, vaya al menú y seleccione **Cancelar servidor**.

## Apagar un servidor
Puede crear un servidor de antemano para prepararse, pero luego apagarlo para asegurarse de que no se modifique nada y de que nadie pueda acceder a él. Cuando esté listo, puede encender el servidor y tenerlo en marcha en cuestión de minutos.
{:shortdesc}

Para apagar el servidor, vaya al menú y seleccione **Encender/Apagar**. Mientras el servidor esté apagado, se incluirá igualmente en la facturación.

**Nota:** si el servidor se ha apagado, permanece en estado apagado y debe encenderlo manualmente.
