---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mit Intel Optane kompatiblen Bare-Metal-Server bereitstellen
Gehen Sie wie folgt vor, um einen Bare-Metal-Server mit Intel Optane-Laufwerk bereitzustellen: 
1. Verwenden Sie die Prozedur [Angepassten Bare-Metal-Server erstellen](../bare-metal/baremetal-provision.html). 
* Wählen Sie im Bestellformular die folgenden Optionen aus: 

|Abschnitt|Auszuwählende Option
|------|------|
|Rechenzentrum|Wählen Sie eines der folgenden Rechenzentren aus, um das Intel Optane-Laufwerk zu verwenden: <br>AMS03 - Amsterdam<br>DAL09 - Dallas<br>DAL10 - Dallas<br>DAL12 - Dallas<br>FRA02 - Frankfurt<br>LON02 - London<br>MEL01 - Melbourne<br>MON01 - Montreal<br>OSL01 - Oslo<br>SJC03 - San José<br>TOR01 - Toronto<br>WDC04 - Washington, DC|
|Server|Die folgenden Server sind mit dem Intel Optane-Laufwerk kompatibel: <br>Intel Xeon 4110 mit bis zu 12 Laufwerken<br>Intel Xeon 5120 mit bis zu 12 Laufwerken<br>Intel Xeon 6140 mit bis zu 12 Laufwerken<br>Intel Xeon E5-2620 v4 mit GPU-Unterstützung<br>Intel Xeon E5-2650 v4 mit GPU-Unterstützung<br>Intel Xeon E5-2690 v4 mit GPU-Unterstützung<br><br>  **Hinweis**: Wenn Sie E5-2620 v4, E5-2650 v4 oder E5-2650 v4 auswählen, ersetzt das Intel Optane-Laufwerk die GPU, sodass Sie nicht sowohl eine GPU als auch ein Intel Optane-Laufwerk verwenden können. |
|PCIe-Komponenten| Wählen Sie als erste und/oder zweite PCIe-Komponente ein Intel Optane-Laufwerk aus. |
|Betriebssystem|Für von Intel zur Verfügung gestellte Optane-Laufwerke sind die folgenden Betriebssysteme von Intel zertifiziert: <br>Windows Server 2016 (alle Editionen)<br>Windows Server 2012 R2 (alle Editionen)<br><br>Für mitgelieferte Open-Source-Laufwerke von anderen Anbietern als Intel wurde die Funktionsfähigkeit überprüft; die Laufwerke sind jedoch nicht zertifiziert: <br>Red Hat Enterprise Linux 7.x (64 Bit)<br>Red Hat Enterprise Linux 6.x (64 Bit).
