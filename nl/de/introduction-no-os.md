---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Die Option "Ohne Betriebssystem"

"Ohne Betriebssystem" ist eine Option, mit der ein Bare-Metal-Server ohne Betriebssystem bestellt wird.

## Wie wird ein Bare-Metal-Server ohne Betriebssystem bestellt?

Geben Sie zunächst eine Bestellung für einen Bare-Metal-Server über [SoftLayer.com](https://www.softlayer.com) oder über das [Kundenportal](https://control.softlayer.com) auf.

1. Wählen Sie **Andere** aus **Systemkonfiguration > Betriebssystem** aus.
2. Wählen Sie **Ohne Betriebssystem** aus.

## Wie wird ein Betriebssystem auf einem Server ohne Betriebssystem installiert?

Es gibt zwei Verfahren, wie ein Betriebssystem auf einem Bare-Metal-Server ohne Betriebssystem installiert wird.

### Option 1: PXE-Server

Ein Bare-Metal-Server ohne Betriebssystem kann so eingerichtet werden, dass das Betriebssystem über ein PXE-Setup gebootet und geladen wird (Informationen unter [Preboot Execution Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment)). Stellen Sie den Bare-Metal-Server einfach in einer Netzumgebung mit einem PXE-Setup bereit (dazu gehört in der Regel die Ausführung eines DHCP- und TFTP-Dämons). Konfigurieren Sie das neue Bare-Metal-Server-BIOS so, dass vom Netzadapter gebootet wird. Damit die Option ohne Betriebssystem ordnungsgemäß funktioniert, muss das PXE-Setup sich in demselben VLAN wie der Bare-Metal-Server befinden oder es muss DHCP-Weiterleitung verwendet werden. 

**Hinweis:** Möglicherweise müssen Sie ein Support-Ticket öffnen, um anzufordern, dass die Switch-Ports im Basismodus umgruppiert werden, damit diese Option funktioniert. Die Ursache dafür ist, dass das PXE-Protokoll keine Kompatibilität mit der Link-Aggregation (d. h. LACP, siehe [Link-Aggregation](http://en.wikipedia.org/wiki/Link_aggregation)) erfordert, die jetzt eine Standardfunktionalität für die Bereitstellung von Redundanz ist. Eine andere Möglichkeit wäre, den Server mit nicht verbundenen Uplinks (keine Link-Aggregation) zu bestellen und diese dann in redundante Uplinks zu ändern, nachdem das Betriebssystem installiert wurde. 

### Option 2: IPMI-Einheit

Installieren Sie ein Betriebssystem auf einem Bare-Metal-Server ohne Betriebssystem, indem Sie über die enthaltene IPMI-Einheit von einem ISO-Image booten. Klicken Sie [hier](mount-iso-bare-metal-server.html), um weitere Informationen zum Booten von einem ISO-Image zu erhalten.
