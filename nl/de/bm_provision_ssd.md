---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mit Intel Optane kompatiblen Bare-Metal-Server bereitstellen
{: #bm-provision-optane-server}

Gehen Sie wie folgt vor, um einen Bare-Metal-Server mit Intel Optane-Laufwerk bereitzustellen:
1. Verwenden Sie die Prozedur [Angepassten Bare-Metal-Server erstellen](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Wählen Sie im Bestellformular die folgenden Optionen aus:

|Abschnitt|Auszuwählende Option
|------|------|
|Region-Rechenzentrum|Wählen Sie eines der folgenden Rechenzentren aus, um das Intel Optane-Laufwerk zu verwenden:<br>Europa - AMS03, FRA02, LON02, OSL01<br>Nordamerika - Süden - DAL09, DAL10, DAL12<br>Asien/Pazifik - MEL01<br>Nordamerika - Osten - MON01, TOR01, WDC04<br>Nordamerika - Westen- SJC03<br>|
|Server|1. Wählen Sie **Alle Server** aus.<br>2. Wählen Sie *Dualprozessoren* aus.<br>3. Wählen Sie einen der folgenden Server aus:<br>-Intel Xeon 4110 mit bis zu 12 Laufwerken<br>-Intel Xeon 5120 mit bis zu 12 Laufwerken<br>-Intel Xeon 6140 mit bis zu 12 Laufwerken<br>-Intel Xeon E5-2620 v4 mit GPU-Unterstützung<br>-Intel Xeon E5-2650 v4 mit GPU-Unterstützung<br>-Intel Xeon E5-2690 v4 mit GPU-Unterstützung<br><br>  **Hinweis**: Wenn Sie E5-2620 v4, E5-2650 v4 oder E5-2650 v4 auswählen, ersetzt das Intel Optane-Laufwerk die GPU, sodass Sie nicht sowohl eine GPU als auch ein Intel Optane-Laufwerk verwenden können.|
|Betriebssystem|Für von Intel zur Verfügung gestellte Optane-Laufwerke sind die folgenden Betriebssysteme von Intel zertifiziert:<br>Windows Server 2016 (alle Editionen)<br>Windows Server 2012 R2 (alle Editionen)<br><br>Für mitgelieferte Open-Source-Laufwerke von anderen Anbietern als Intel wurde die Funktionsfähigkeit überprüft; die Laufwerke sind jedoch nicht zertifiziert:<br>Red Hat Enterprise Linux 7.x (64 Bit)<br>Red Hat Enterprise Linux 6.x (64 Bit).
|Image-Add-ons| Wählen Sie als erste und/oder zweite PCIe-Komponente ein Intel Optane-Laufwerk aus.|
