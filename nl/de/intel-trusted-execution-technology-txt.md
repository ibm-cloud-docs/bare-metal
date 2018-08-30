---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Hardwareüberwachung und Sicherheitsmaßnahmen

Durch die Erhöhung bösartiger Bedrohungen müssen Sie strengere Sicherheitsanforderungen einhalten und jeden Aspekt Ihrer Ausführungsumgebung genau prüfen. Sie erwarten von Ihren Cloud-Providern eine Hardwareüberwachung und Sicherheitsmaßnahmen, mit denen ermittelt werden kann, ob eine Workload auf vertrauenswürdiger Hardware an einem bekannten Speicherort ausgeführt wird. {{site.data.keyword.cloud}} bietet Ihnen die Möglichkeit, Hybrid- und Cloudumgebungen mit erweiterter Sicherheitsüberprüfung in Ihrer Startumgebung zu implementieren. Dazu wird die &reg; Trusted Execution Technology (Intel&reg; TXT) genutzt.
{:shortdesc}

## Funktionsweise

Intel TXT stellt Hardwareüberwachung und Sicherheitsmaßnahmen bereit, mit denen Unternehmen sicherstellen können, dass eine implementierte oder in eine {{site.data.keyword.cloud_notm}}-Infrastruktur migrierte Workload auf vertrauenswürdiger Hardware an einem bekannten Speicherort ausgeführt wird. {{site.data.keyword.cloud_notm}} unterstützt Intel TXT auf einer Reihe von {{site.data.keyword.baremetal_short}}. Die vollständige Liste finden Sie unter "http://www.softlayer.com/intel-txt".

Intel TXT analysiert und misst die Komponenten eines Computersystems vom Betriebssystem oder Hypervisor zur Bootfirmware und -hardware des Computersystems. Die Analyse umfasst das BIOS (Basic Input/Output System), den Master-Bootsatz (MBR) und das Bootladeprogramm. Die Messwerte werden mit einer Standard-Baseline verglichen, um festzustellen, ob das System vertrauenswürdig ist. Systemsoftware und lokale oder Fernverwaltungssoftware können die Vertrauensentscheidung verwenden, um das Ausführen einer Arbeitslast auf diesem Computersystem zuzulassen oder zu verweigern. Da Intel TXT die Analyse und die Messung während des Hochfahrens durchführt, führt die hinzugefügte Sicherheit bei den Anwendungen nicht zu Leistungseinbußen.

Die Baseline-Messwerte werden auf einer Trusted Platform Module (TPM)-Hardwareeinheit gespeichert. Die TPM-Einheit ist im Serversystem integriert und bietet eine Reihe von Intel TXT-sicherheitsrelevante Funktionen.

## Ihre Vorteile

Intel TXT ist besonders für große Unternehmen vorteilhaft, die Compliance- und Audit-Vorschriften einhalten müssen, wie z. B. im Gesundheitswesen, bei Finanzdienstleistungen und für Regierungsbehörden. Es wird sichergestellt, dass die Überwachung aller vertrauenswürdigen Ressourcen integriert und verwaltet sowie an die an die entsprechenden Compliance-Organisationen (HIPAA, PCI, FedRAMP, ISO, FISMA und SSAE 16) weitergegeben werden. Erstmalig können diese Organisationen ein Cloud-Computing-System zertifizieren, das eine angemessene Sicherheit für Workloads wie die folgenden bietet: 

* Governance und Unternehmensrisiken
* Informations- und Lebenszyklusmanagement
* Compliance und Audit
* Anwendungssicherheit
* Identitäts- und Zugriffsmanagement
* Behebung von Störfällen

Weitere Informationen zu Intel TXT auf {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} finden Sie unter http://www.softlayer.com/intel-txt. 

Unter dem folgenden Link finden Sie weitere Informationen dazu, wie Sie die Sicherheit und Compliance für Ihre Workloads mit einer [vertrauenswürdigen, sicheren Cloudlösung von IBM, VMware und HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf) verbessern können. 

**Spezieller technischer Hinweis** Intel Trusted Execution Technology (Intel TXT) wird von Intel&reg; bereitgestellt und ist in {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} enthalten, für deren Unterstützung und Verwaltung spezielles technisches Wissen notwendig ist. Beim aktuellen Bereitstellungsmodell von {{site.data.keyword.cloud_notm}} kann Intel TXT entweder aktiviert oder inaktiviert werden. **{{site.data.keyword.cloud_notm}} kann die Konfiguration von Intel TXT-Einstellungen aufgrund der Vertraulichkeit von Kundenumgebungen und Daten nicht unterstützen**. Es wird empfohlen, entweder Mitarbeiter einzusetzen, die für Intel TXT-Technologien geschult wurden, oder mit einem Beratungsunternehmen zusammenzuarbeiten, das über fundierte Kenntnisse in der Orchestrierung von Root-of-Trust- und MLE-Architekturen (Measured Launch Environment) verfügt. 
