---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# Die Option "Ohne Betriebssystem"
{: #bm-no-os}

**Ohne Betriebssystem** ist eine Option, mit der ein {{site.data.keyword.baremetal_long}} ohne Betriebssystem bestellt wird.

## {{site.data.keyword.baremetal_short}} ohne Betriebssystem bestellen
{: #ordering-no-os}

1. Führen Sie die Schritte aus, die in [Angepassten Bare-Metal-Server erstellen](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) beschrieben werden, um Ihren Server zu bestellen.
2. Wählen Sie **Ohne Betriebssystem** unter **Image** aus.
3. Vervollständigen Sie Ihre Serverbestellung. 

## Änderung in 'Ohne Betriebssystem'
{: #changing-to-no-os}

Ein Server kann ohne Betriebssystem neu konfiguriert werden. Die Rekonfiguration wird über ein erneutes Laden des Betriebssystems ausgeführt. Weitere Informationen finden Sie unter [Betriebssystem erneut laden](/docs/infrastructure/software?topic=software-reloading-the-os).

1. Klicken Sie auf **Einheiten** > **Einheitenliste**.
2. Wählen Sie den Server aus, der ohne Betriebssystem neu konfiguriert werden soll. 
3. Klicken Sie auf **Erneutes Laden des Betriebssystems** und geben Sie die zutreffenden Informationen ein.

## Betriebssystem auf einem Server ohne Betriebssystem installieren
{: #installing-os-on-no-os-server}

Es gibt zwei Methoden zum Installieren von Betriebssystemen auf {{site.data.keyword.baremetal_short}}-Instanzen ohne Betriebssystem.

### Option 1: PXE-Server
{: #option-1}

{{site.data.keyword.baremetal_short}}-Instanzen ohne Betriebssystem können so eingerichtet werden, dass das Betriebssystem über ein PXE-Setup gebootet und geladen wird.<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> Stellen Sie {{site.data.keyword.baremetal_short}} in einer Netzumgebung mit einem PXE-Setup bereit (dazu gehört in der Regel die Ausführung eines DHCP- und TFTP-Dämons). Konfigurieren Sie das BIOS der neuen Server so, dass vom Netzadapter gebootet wird. Damit die Option ohne Betriebssystem ordnungsgemäß funktioniert, muss das PXE-Setup sich in demselben VLAN wie die {{site.data.keyword.baremetal_short}}-Instanz befinden oder es muss DHCP-Weiterleitung verwendet werden.

Möglicherweise müssen Sie ein Support-Ticket öffnen, um anzufordern, dass die Switch-Ports im Basismodus umgruppiert werden, damit diese Option funktioniert. Die Ursache dafür ist, dass das PXE-Protokoll keine Kompatibilität mit der Link-Aggregation <!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> erfordert, die jetzt eine Standardfunktionalität für die Bereitstellung von Redundanz ist. Eine andere Möglichkeit wäre, den Server mit nicht verbundenen Uplinks (keine Link-Aggregation) zu bestellen und diese dann in redundante Uplinks zu ändern, nachdem das Betriebssystem installiert wurde.
{: note}

### Option 2: IPMI-Einheit
{: #option-2}

Installieren Sie Betriebssysteme auf {{site.data.keyword.baremetal_short}}-Instanzen ohne Betriebssystem, indem Sie über die enthaltene IPMI-Einheit von einem ISO-Image booten. Weitere Informationen zum Booten von einem ISO-Image finden Sie unter [Ein ISO-Image an einen Bare-Metal-Server anhängen](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server).
