---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Die Option "Ohne Betriebssystem"

"Ohne Betriebssystem" ist eine Option, mit der ein Bare-Metal-Server ohne Betriebssystem bestellt wird.

## Wie wird ein Bare-Metal-Server ohne Betriebssystem bestellt?

Geben Sie zunächst eine Bestellung für einen Bare-Metal-Server über [SoftLayer.com](softlayer.com) oder über das [Kundenportal](https://control.softlayer.com) auf.

1. Wählen Sie **Andere** aus **Systemkonfiguration > Betriebssystem** aus.
2. Wählen Sie **Ohne Betriebssystem** aus.

## Wie wird ein Betriebssystem auf einem Server ohne Betriebssystem installiert?

Es gibt zwei Verfahren, wie ein Betriebssystem auf einem Bare-Metal-Server ohne Betriebssystem installiert wird.

### Option 1: PXE-Server

Ein Bare-Metal-Server ohne Betriebssystem kann so eingerichtet werden, dass das Betriebssystem über ein PXE-Setup gebootet und geladen wird (Informationen unter [Preboot Execution Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment)). Stellen Sie den Bare-Metal-Server einfach in einer Netzumgebung mit einem PXE-Setup bereit (dazu gehört in der Regel die Ausführung eines DHCP- und TFTP-Dämons). Konfigurieren Sie das neue Bare-Metal-Server-BIOS so, dass vom Netzadapter gebootet wird. Damit das richtig funktioniert, muss sich das PXE-Setup im selben VLAN wie das PXE-Setup befinden oder die DHCP-Weiterleitung verwendet werden.

**Hinweis:** Es ist ggf. notwendig, ein Support-Ticket zu öffnen, um zu beantragen, dass die Switch-Ports im Basismodus umgruppiert werden, damit diese Option funktioniert. Dies liegt an der Tatsache, dass das PXE-Protokoll nicht mit der Link-Aggregation kompatibel sein muss (z. B. LACP, siehe [Link-Aggregation](http://en.wikipedia.org/wiki/Link_aggregation)), die jetzt eine Standardfunktionalität für die Bereitstellung von Redundanz ist. Eine andere Möglichkeit wäre, den Server mit nicht verbundenen Uplinks (keine Link-Aggregation) zu bestellen und diese dann in redundante Uplinks zu ändern, sobald das Betriebssystem installiert wurde.

### Option 2: IPMI-Einheit

Installieren Sie ein Betriebssystem auf einem Bare-Metal-Server ohne Betriebssystem, indem Sie über die enthaltene IPMI-Einheit von einem ISO-Image booten. Klicken Sie [hier](mount-iso-bare-metal-server.html), um weitere Informationen zum Booten von einem ISO-Image zu erhalten.
