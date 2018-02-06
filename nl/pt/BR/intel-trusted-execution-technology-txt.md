---



copyright:
  years: 1994, 2017
lastupdated: "2017-11-24"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Monitoramento de hardware e controles de segurança

A escalada e a sofisticação de ameaças maliciosas têm feito você empregar requisitos de segurança mais rigorosos e examinar cada aspecto do seu ambiente de execução. Você está procurando seus provedores em nuvem para oferecer monitoramento de hardware e controles de segurança que podem determinar se uma carga de trabalho está em execução no hardware confiável em um local conhecido. O {{site.data.keyword.cloud}} está liderando o caminho, permitindo que você implemente ambientes híbridos e nuvem com verificação de segurança aprimorada do seu ambiente de ativação usando o Intel&reg; Trusted Execution Technology (Intel&reg; TXT). {:shortdesc}

## Como ele funciona

O Intel TXT fornece monitoramento de hardware e controles de segurança que ajudam a assegurar que os negócios que uma carga de trabalho implementou ou migrou para a infraestrutura do {{site.data.keyword.cloud_notm}} estejam em execução em hardware confiável em um local conhecido. O {{site.data.keyword.cloud_notm}} fornece suporte para o Intel TXT em uma gama de {{site.data.keyword.baremetal_short}}. Veja http://www.softlayer.com/intel-txt para obter uma lista completa.

O Intel TXT analisa e mede os componentes de um sistema de cálculo do sistema operacional ou hypervisor para o firmware de inicialização e o hardware do sistema de cálculo. A análise inclui o basic input/output system (BIOS) do sistema, o master boot record (MBR) e o carregador de inicialização. As medidas são comparadas a uma linha de base padrão para determinar se o sistema é confiável ou não confiável. O software do sistema e o software de gerenciamento local ou remoto podem usar a decisão de confiança para permitir ou negar que uma carga de trabalho seja executada nesse sistema de cálculo. Como o Intel TXT executa a análise e medição durante a inicialização, a segurança incluída não inclui nenhuma sobrecarga de desempenho para aplicativos.

As medições de linha de base são armazenadas no dispositivo de hardware Trusted Platform Module (TPM). O dispositivo TPM está integrado no sistema do servidor e fornece uma gama de funções relacionadas à segurança do Intel TXT.

## O que ele faz por você

O Intel TXT é especialmente vantajoso para grandes empresas sujeitas a regulamentações de conformidade e auditoria, como assistência médica, serviços financeiros e organizações governamentais. E ajuda a assegurar que o rastreamento de todos os recursos confiáveis possa ser integrado, gerenciado e relatado com as organizações de conformidade relevantes (HIPAA, PCI, FedRAMP, ISO, FISMA e SSAE 16). Pela primeira vez, essas organizações poderão certificar se um sistema de computação em nuvem está protegido adequadamente para cargas de trabalho como

* Controle e risco corporativo
* Gerenciamento de informações e ciclo de vida
* Conformidade e auditoria
* Segurança do aplicativo
* Identidade e gerenciamento de acesso
* Resposta de incidente

Para obter mais informações sobre o Intel TXT em {{site.data.keyword.baremetal_short}} {{site.data.keyword.cloud_notm}}, visite http://www.softlayer.com/intel-txt.

O link a seguir tem mais informações sobre como incluir segurança adicional e conformidade para suas cargas de trabalho com uma [solução de nuvem segura confiável com a IBM, VMware e HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf).

**Aviso técnico especial** O Intel Trusted Execution Technology (Intel TXT) é fornecido pela Intel&reg; e opera nos {{site.data.keyword.baremetal_short}} {{site.data.keyword.cloud_notm}} que requerem conhecimento técnico específico para suporte e gerenciamento. O modelo de entrega atual do {{site.data.keyword.cloud_notm}} permite transformar ativar ou desativar o Intel TXT; o **{{site.data.keyword.cloud_notm}} não pode ajudar com a definição de configurações do Intel TXT devido ao sigilo de ambientes e dados do cliente**. É recomendado que você também tenha uma equipe treinada em tecnologias TXT da Intel ou se envolva com uma firma de consultoria com conhecimento comprovado em orquestrar a raiz de confiança e a arquitetura measured launch environment (MLE).
