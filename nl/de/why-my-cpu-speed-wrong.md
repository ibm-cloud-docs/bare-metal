---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Warum stimmt die CPU-Geschwindigkeit nicht?

Wenn Sie sich bei einem Server anmelden, um die CPU-Informationen zu prüfen, stellen Sie fest, dass die Geschwindigkeit der Prozessoren falsch war. Diese Abweichung kann an Enhanced Intel SpeedStep Technology (EIST) liegen. EIST ist der Intel-Name für die Technologie der dynamischen Skalierungstechnologie. Diese Technologie heißt auch *CPU-Drosselung* oder in älteren Systemen *Bus Slewing*. In einigen AMD-Systemen gibt es ähnliche Technologien, die *Cool'N'Quiet* oder *PowerNow!* heißen. Obwohl sie nicht alle exakt dieselbe Technologie darstellen, haben Sie doch dasselbe Ziel. Der Stromverbrauch und die Hitzeentwicklung sollen gesenkt werden, wenn der Prozessor nicht stark beansprucht wird, indem die CPU-Geschwindigkeit verlangsamt wird. Wenn der Server wieder eine Last verarbeitet, wird die Taktgeschwindigkeit wieder erhöht. 

Wenn Sie wissen möchte, ob der Intel-Prozessor Ihres Servers SpeedStep unterstützt, besuchen Sie das Kundenportal: 
1. Klicken Sie auf **Einheiten**.
* Ermitteln Sie Ihren Server in der Liste.
* Klicken Sie auf den Servernamen, um **Einheitendetails** anzuzeigen.
* Suchen Sie den Teilbereich mit dem Namen **Hardware**, um die Modellnummer Ihres Serverprozessors für die CPU-Geschwindigkeit zu suchen.
* Notieren Sie sich die Modellnummer des Serverprozessors. Gehen Sie zum [Intel Processor Finder](http://processorfinder.intel.com/) und suchen Sie mit dieser Nummer nach weiteren Informationen zum Prozessor und zur Angabe, ob Enhanced Intel SpeedStep Technology (EIST) unterstützt wird.

EIST ist eine bewährte Technologie. Es gibt keinen Grund, EIST zu inaktivieren. Wenn Sie jedoch entscheiden, dass Sie diese Funktion nicht nutzen möchten, öffnen Sie ein Ticket beim Support-Team, um die Funktion inaktivieren zu lassen. Um diese Funktion zu inaktivieren, muss der Server neu gestartet werden.
