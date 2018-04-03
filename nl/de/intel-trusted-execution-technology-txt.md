---



copyright:
  years: 1994, 2017
lastupdated: "2017-11-24"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Hardwareüberwachung und Sicherheitsmaßnahmen

Durch die Erhöhung bösartiger Bedrohungen müssen Sie strengere Sicherheitsanforderungen einhalten und jeden Aspekt Ihrer Ausführungsumgebung genau prüfen. Sie erwarten von Ihren Cloud-Providern eine Hardwareüberwachung und Sicherheitsmaßnahmen, mit denen ermittelt werden kann, ob eine Workload auf vertrauenswürdiger Hardware an einem bekannten Speicherort ausgeführt wird. {{site.data.keyword.cloud}} bietet Ihnen die Möglichkeit, Hybrid- und Cloudumgebungen mit erweiterter Sicherheitsüberprüfung in Ihrer Startumgebung zu implementieren. Dazu wird die Intel&reg; Trusted Execution Technology (Intel&reg; TXT) genutzt. {:shortdesc}

## Funktionsweise

Intel TXT stellt Hardwareüberwachung und Sicherheitsmaßnahmen bereit, mit denen sichergestellt werden kann, dass eine bereitgestellte oder in eine {{site.data.keyword.cloud_notm}}-Infrastruktur migrierte Workload auf vertrauenswürdiger Hardware an einem bekannten Speicherort ausgeführt wird. {{site.data.keyword.cloud_notm}} unterstützt Intel TXT für viele {{site.data.keyword.baremetal_short}}. Die vollständige Liste finden Sie unter "http://www.softlayer.com/intel-txt".

Intel TXT analysiert und misst die Komponenten eines Computersystems vom Betriebssystem oder Hypervisor zur Bootfirmware und -hardware des Computersystems. Die Analyse umfasst das BIOS (Basic Input/Output System), den Master-Bootsatz (MBR) und das Bootladeprogramm. Die Messwerte werden mit einer Standard-Baseline verglichen, um festzustellen, ob das System vertrauenswürdig ist. Systemsoftware und lokale oder Fernverwaltungssoftware können die Vertrauensentscheidung verwenden, um das Ausführen einer Arbeitslast auf diesem Computersystem zuzulassen oder zu verweigern. Da Intel TXT die Analyse und die Messung während des Hochfahrens durchführt, führt die hinzugefügte Sicherheit bei den Anwendungen nicht zu Leistungseinbußen.

Die Baseline-Messwerte werden auf einer Trusted Platform Module (TPM)-Hardwareeinheit gespeichert. Die TPM-Einheit ist im Serversystem integriert und bietet eine Reihe von Intel TXT-sicherheitsrelevante Funktionen.

## Ihre Vorteile

Intel TXT ist besonders für große Unternehmen vorteilhaft, die Compliance- und Audit-Vorschriften einhalten müssen, wie z. B. im Gesundheitswesen, bei Finanzdienstleistungen und für Regierungsbehörden. Es wird sichergestellt, dass die Überwachung aller vertrauenswürdigen Ressourcen integriert und verwaltet sowie an die an die entsprechenden Compliance-Organisationen (HIPAA, PCI, FedRAMP, ISO, FISMA und SSAE 16) weitergegeben werden. Erstmalig können diese Organisationen ein Cloud-Computing-System zertifizieren, das für Workloads angemessen gesichert ist, wie:

* Governance und Unternehmensrisiken
* Informations- und Lebenszyklusmanagement
* Compliance und Audit
* Anwendungssicherheit
* Identitäts- und Zugriffsmanagement
* Behebung von Störfällen

Weitere Informationen zu Intel TXT in {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}n finden Sie unter "http://www.softlayer.com/intel-txt".

Unter dem folgenden Link finden Sie weitere Informationen, wie eine höhere Sicherheit und Compliance für Ihre Workload mit einer [vertrauenswürdigen, sicheren Cloudlösung von IBM, VMware und HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf) implementiert werden kann.

**Spezieller technischer Hinweis** Intel Trusted Execution Technology (Intel TXT) wird von Intel&reg; bereitgestellt und ist in {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}n enthalten. Für den Support und die Verwaltung ist spezifisches Wissen notwendig. Mit dem aktuellen {{site.data.keyword.cloud_notm}}-Übermittlungsmodell kann Intel TXT aktiviert oder inaktiviert werden. **{{site.data.keyword.cloud_notm}} kann die Konfiguration von Intel TXT-Einstellungen aufgrund der Sicherheitsstufe von Kundenumgebungen und Daten nicht unterstützen**. Es wird empfohlen, Mitarbeiter in den Intel TXT-Technologien zu schulen oder mit einem Beratungsunternehmen zusammenzuarbeiten, das fundierte Kenntnisse in der Orchestrierung von Root-of-Trust- und Measured Launch Environment (MLE)-Architekturen hat.
