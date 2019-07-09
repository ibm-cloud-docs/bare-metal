---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-31"

keywords: bare metal, intel txt

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Surveillance du matériel et contrôles de sécurité
{: #bm-hardware-monitroing-security-controls}

La recrudescence et la sophistication des menaces malveillantes vous ont obligé à employer des exigences de sécurité plus rigoureuses et à étudier de près chaque aspect de votre environnement d'exécution. Vous vous tournez vers vos fournisseurs de cloud pour offrir une surveillance du matériel et des contrôles de sécurité qui peuvent déterminer si une charge de travail est en cours d'exécution sur du matériel digne de confiance à un emplacement connu. {{site.data.keyword.cloud}} ouvre la voie en vous permettant de déployer des environnements de cloud et hybrides avec une vérification de la sécurité renforcée pour votre environnement de lancement via la technologie Intel&reg; TXT (Intel&reg; Trusted Execution Technology). {:shortdesc}

## Fonctionnement

Intel TXT fournit une surveillance du matériel et des contrôles de sécurité qui permettent aux entreprises de s'assurer qu'une charge de travail déployée sur ou migrée vers l'infrastructure {{site.data.keyword.cloud_notm}} est en cours d'exécution sur du matériel digne de confiance à un emplacement connu. {{site.data.keyword.cloud_notm}} prend en charge Intel TXT sur une gamme de serveurs {{site.data.keyword.baremetal_short}}. Pour obtenir une liste complète, voir [Intel Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt).

Intel TXT analyse et mesure les composants d'un système informatique à partir du système d'exploitation ou de l'hyperviseur vers le microprogramme d'amorçage et le matériel du système informatique. L'analyse inclut le système BIOS, le secteur de démarrage principal et le chargeur de démarrage du système. Les mesures sont comparées à une base de référence standard afin de déterminer si le système est digne de confiance ou non. Le logiciel système et le logiciel de gestion à distance ou locale peuvent utiliser la décision d'approbation pour autoriser ou refuser l'exécution d'une charge de travail sur ce système informatique. Etant donné qu'Intel TXT effectue l'analyse et la mesure durant l'amorçage, la sécurité ajoutée ne dégrade pas les performances des applications.

Les mesures de base de référence sont stockées sur une unité matérielle TPM (Trusted Platform Module). L'unité TPM est intégrée au système serveur et fournit une gamme de fonctions de sécurité Intel TXT.

## Avantages

La technologie Intel TXT est particulièrement avantageuse pour les grandes entreprises soumises à des réglementations de conformité et d'audit, telles que des établissements de soins de santé, des services financiers et des organisations gouvernementales. Elle permet de s'assurer que le suivi de toutes les ressources dignes de confiance peut être intégré à, géré avec et signalé auprès des organismes de conformité compétents (HIPAA, PCI, FedRAMP, ISO, FISMA et SSAE 16). Pour la première fois, ces organismes sont en mesure de certifier qu'un système cloud computing est correctement sécurisé pour les charges de travail, telles que les suivantes :

* Gouvernance et risque d'entreprise
* Gestion des informations et du cycle de vie
* Conformité et audit
* Sécurité des applications
* Gestion des identités et des accès
* Réaction aux incidents

Pour plus d'informations sur Intel TXT sur {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}, voir [Intel Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt).

Le lien suivant permet d'accéder à davantage d'informations sur l'ajout supplémentaire de sécurité et de conformité à vos charges de travail à l'aide d'une [solution cloud sécurisée avec IBM, VMware et HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf).

**Notice technique spéciale** : La technologie Intel TXT (Intel Trusted Execution Technology) est fournie par Intel et fonctionne sur des serveurs {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} dont la prise en charge et la gestion nécessitent une connaissance technique spécifique. Le modèle de distribution actuel pour {{site.data.keyword.cloud_notm}} peut activer ou désactiver Intel TXT ; **{{site.data.keyword.cloud_notm}} ne peut pas aider à la configuration des paramètres Intel TXT en raison de la sensibilité des environnements et des données client.**. Il est recommandé d'inclure du personnel formé aux technologies Intel TXT ou de coopérer avec un cabinet d'experts-conseils ayant une expertise avérée dans l'orchestration de la racine de confiance et l'architecture MLE (environnement de lancement mesuré).
