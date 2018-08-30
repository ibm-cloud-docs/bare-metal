---

copyright:

  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Bare Metal Server einrichten
{: #customerportal_setupbaremetal}

Sie können einen Bare Metal Server als dedizierten Server einrichten.
{:shortdesc}

Führen Sie die folgenden Schritte aus, um einen Bare Metal Server einzurichten: 

1. Melden Sie sich mit Ihren eindeutigen Berechtigungsnachweisen beim {{site.data.keyword.BluSoftlayer_full}}-Kundenportal an. 

2. Im Menü klicken Sie auf **Einheiten** > **Einheitenliste** und suchen Sie Ihr System. Alle Ihre Einheiten sind in der Einheitenliste aufgeführt. In dieser Liste können Sie Einheiten verwalten, Einheiten aktualisieren oder Diagramme für die Bandbreitennutzung generieren. 

3. Verwalten Sie Ihren Server mit einer der folgenden Methoden: 
  * Klicken Sie auf den Pfeil neben dem Einheitennamen, um eine Zusammenfassung anzuzeigen und Ihre Einheiten in der Snapshotansicht zu verwalten. 
  * Klicken Sie auf den Einheitennamen des Servers, um eine detaillierte Liste anzuzeigen und die Einheiten in der Anzeige "Einheitendetails" zu verwalten. 

4. Notieren Sie die IP-Adresse und die Berechtigungsnachweise für den Server an einem sicheren Ort, sodass Sie schnell auf die Details zugreifen können, ohne dass Sie sich jedes Mal im Kundenportal anmelden müssen, wenn Sie die Details benötigen. Sie können diese Details sowohl für eine einzelne Einheit als auch für alle Einheiten notieren, die Ihrem Konto zugeordnet sind: 
  * Zeigen Sie die IPs für einzelne Einheiten in der Einheitenliste an. 
  * Zeigen Sie die Rootkennwörter für einzelne Einheiten in der Snapshotansicht für die Einheit an. 
  * Zeigen Sie die IPs mehrerer Einheiten unter Verwendung der Option **CSV herunterladen** in der **Einheitenliste** an. Wählen Sie anschließend **CSV herunterladen** unter **Einstellungen** aus, um eine vollständige Liste der Einheiten und Details im Tabellenformat herunterzuladen. 

5. Aktualisieren Sie die Berechtigungsnachweise für Betriebssysteme und sonstige Software. Allen Programmen, die während des Bereitstellungsprozesses auf Ihre Einheit geladen wurden, wurden temporäre Berechtigungsnachweise zugeordnet. Sie können diese Berechtigungsnachweise auf der Registerkarte "Kennwörter" jeder Einheit im Kundenportal anzeigen und verwalten. Verwenden Sie diese temporären Berechtigungsnachweise, um zum ersten Mal auf Ihre Software zuzugreifen, und ändern Sie anschließend das Kennwort für Ihre Software in ein starkes Kennwort, das aus einer Kombination aus Buchstaben, Zahlen und Symbolen besteht. Optional können Sie Kennwortaktualisierungen auf der Registerkarte "Kennwörter" für jede Einheit speichern. Wenn Sie jedoch Kennwörter im Kundenportal speichern, können alle Personen mit Zugriff auf das Konto und den entsprechenden Berechtigungen die Kennwörter anzeigen, die in der Anzeige "Kennwörter" gespeichert sind. 

6. Greifen Sie im privaten Netz auf Ihren Server zu. Sie können das private Netz der {{site.data.keyword.BluSoftlayer_notm}}-Infrastruktur verwenden, um über Remote Desktop (RDP) mit SSH und KVM über IP mit Ihren Einheiten zu interagieren. Sie können das VPN-Zugriffstool für die private Netzverbindung zum nächsten SSL-VPN-Endpunkt oder zum Endpunkt Ihrer Wahl verwenden. VPN-Zugriff ist auch erforderlich, um mit mehreren Services zu interagieren. Wenn Sie auf das private Netz zugreifen möchten, bearbeiten Sie den VPN-Zugriff des Benutzers in der Benutzerliste. Für den Zugriff auf die Benutzerliste klicken Sie auf **Konto** > **Benutzer** > **Benutzerliste**. Verwenden Sie die Seite [Virtual Private Network ![Symbol für externen Link](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window}, um eine Verbindung zu einer der verschiedenen VPN-Optionen herzustellen. 

7. Richten Sie die Überwachung ein, um den Status des Servers zu überprüfen, damit Sie wissen, wann Sie ihn skalieren müssen. Sie können entweder die Standardüberwachung oder Nimsoft-Überwachungsservices verwenden. Bei der Standardüberwachung (oder Basisüberwachung) mit der Ping-und-Antwort-Methode wird ein langsames Pingsignal oder ein Servicepingsignal vom Kundenportal verwendet. Sie können auch die Nimsoft-Überwachung oder die erweiterte Überwachung aus dem Kundenportal oder in einer von drei möglichen Stufen verwenden: Basis, Erweitert und Premium. 

8. Schützen Sie Ihr System. Verwenden Sie die verfügbaren Hardware-Firewalls, um sicherzustellen, dass Ihre Einheit immer sicher ist. Sie können Hardware-Firewalls auf Anforderung ohne Ausfallzeit bereitstellen, wenn Regeln ordnungsgemäß eingerichtet werden, um Ihren Server vor unerwünschten Aktivitäten zu schützen. Nachdem Sie Ihre Firewall bestellt haben, muss sie aktiviert und die Regeln müssen definiert werden. 

9. Planen Sie Sicherungen, um sicherzustellen, dass Ihre Daten sicher außerhalb Ihrer Einheit gespeichert sind, damit Sie sie erneut laden können, wenn sie verloren gehen. Sie können aus einer Vielzahl von Sicherungsservices auswählen, um Ihre Daten an einem sicheren Ort zu speichern: 
  * EVault Backup ist ein automatisiertes, agentenbasiertes Sicherungssystem. Dies ist eine vielfach eingesetzte "Set-and-forget"-Lösung für die Verwaltung Ihrer Einheit. Mit zusätzlichen Plug-ins ist sie mit Microsoft-Software einschließlich Exchange und SQL kompatibel. EVault-Benutzer interagieren mit diesem Service über die webbasierte EVault-Anwendung WebCC. 
  * R1Soft Continuous Data Protection (CDP) kann auf Ihrem Server oder Ihrer selbstverwalteten virtuellen Maschine installiert werden. Dies wird empfohlen, wenn Sie eine einzige Schnittstelle für die Verwaltung aller Ihrer Sicherungen suchen. Sie interagieren mit R1Soft CDP über Ihr proprietäres Managementsystem, mit dem Agenten auf virtuellen Maschinen installiert werden können und das Datenbank-Plug-ins für zusätzliche Funktionalität bietet. 
