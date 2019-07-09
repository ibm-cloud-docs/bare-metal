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

# Controles de seguridad y supervisión de hardware
{: #bm-hardware-monitroing-security-controls}

El aumento y la sofisticación de las amenazas maliciosas le obliga a aplicar requisitos de seguridad más estrictos y analizar al detalle todos los aspectos del entorno de ejecución. Espera que los proveedores de nube ofrezcan controles de seguridad y supervisión de hardware que puedan determinar si una carga de trabajo se ejecuta en hardware de confianza en una ubicación conocida. En {{site.data.keyword.cloud}} son pioneros en este sentido, ya que permiten desplegar entornos híbridos y de nube con una verificación de seguridad mejorada del entorno de lanzamiento mediante Intel&reg; Trusted Execution Technology (Intel&reg; TXT). {:shortdesc}

## Cómo funciona

Intel TXT proporciona controles de seguridad y supervisión de hardware que permiten garantizar a las empresas que una carga de trabajo que se ha desplegado o migrado a la infraestructura de {{site.data.keyword.cloud_notm}} se ejecuta en hardware de confianza en una ubicación conocida. {{site.data.keyword.cloud_notm}} da soporte a Intel TXT en diversos {{site.data.keyword.baremetal_short}}. Consulte [Intel Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt) para obtener una lista completa.

Intel TXT analiza y mide los componentes de un sistema informático desde el sistema operativo o el hipervisor hasta el firmware y el hardware de arranque del sistema informático. El análisis incluye el sistema básico de entrada/salida (BIOS), el registro de arranque principal (MBR) y el cargador de arranque del sistema. Las medidas se comparan con una referencia estándar para determinar si el sistema es de confianza o no. El software del sistema y el software de gestión local o remota pueden utilizar esta decisión para permitir o rechazar que una carga de trabajo se ejecute en dicho sistema informático. Puesto que Intel TXT realiza el análisis y la medición durante el arranque, esta seguridad añadida no sobrecarga el rendimiento de las aplicaciones.

Las medidas de referencia se almacenan en un dispositivo de hardware TPM (módulo de plataforma de confianza). El dispositivo TPM está integrado en el sistema del servidor y proporciona una serie de funciones relacionadas con la seguridad de Intel TXT.

## Qué hace por usted

Intel TXT beneficia especialmente a las grandes empresas, que están sujetas a normativas de auditoría y conformidad relacionadas con la sanidad, los servicios financieros o los organismos públicos. Permite garantizar que el seguimiento de todos los recursos de confianza se pueda integrar, gestionar y notificar con las organizaciones de cumplimiento pertinentes (HIPAA, PCI, FedRAMP, ISO, FISMA y SSAE 16). Por primera vez, estas organizaciones pueden certificar que un sistema de computación en la nube ofrece una protección adecuada para cargas de trabajo como, por ejemplo:

* Gobierno y riesgo empresarial
* Gestión del ciclo de vida e información
* Conformidad y auditoría
* Seguridad de aplicación
* Gestión de identidad y acceso
* Respuesta a incidentes

Para obtener más información sobre Intel TXT en {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}, consulte [Intel Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt).

El enlace siguiente tiene más información sobre cómo añadir más seguridad y conformidad a las cargas de trabajo con una [solución de nube segura y de confianza con IBM, VMware e HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf).

**Aviso técnico especial**: la tecnología Intel Trusted Execution Technology (Intel TXT) la proporciona Intel&reg; y funciona en los {{site.data.keyword.baremetal_short}} de {{site.data.keyword.cloud_notm}} que requieren conocimientos técnicos específicos para su soporte y gestión. El modelo de entrega actual de {{site.data.keyword.cloud_notm}} puede activar o desactivar Intel TXT; **{{site.data.keyword.cloud_notm}} no puede ayudar con los valores de configuración de Intel TXT debido a la confidencialidad de los datos y los entornos de cliente**. Se recomienda incluir personal formado en tecnologías Intel TXT o colaborar con una empresa consultora con experiencia probada en coordinar arquitecturas de MLE (entorno de lanzamiento medido) y raíz de confianza.
