---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Por que a velocidade da CPU está errada?

Se você efetuar login em um servidor para verificar as informações da CPU e observar que a velocidade dos processadores estava incorreta. Essa discrepância pode ser devido a Enhanced Intel SpeedStep Technology (EIST). EIST é o nome Intel para a tecnologia de ajuste de escala de frequência dinâmica.  Essa tecnologia também é chamada de *regulagem de CPU* ou *giro de barramento* em sistemas mais velhos.  Em alguns sistemas AMD, existem tecnologias semelhantes que são chamadas *Cool'N'Quiet* ou *PowerNow!*.  Embora estas tecnologias não sejam todas iguais, elas têm o mesmo objetivo, que é reduzir o consumo de energia e de produção de calor quando o processador não estiver sob uso pesado reduzindo a velocidade de CPU.  Quando o servidor estiver de volta sob carga, ele aumentará a velocidade do clock conforme necessário.

Se você gostaria de saber se o processador Intel em seu servidor suporta SpeedStep, portal do cliente: 
1. Clique em **Dispositivos**.
* Identifique o seu servidor na lista.
* Clique no nome do servidor para visualizar **Detalhes do dispositivo**.
* Localize a subseção intitulada **Hardware** para localizar o número do modelo de sua velocidade de CPU de processadores do servidor.
* Com o número do modelo do processador do servidor, acesse o [Intel Processor Finder](http://processorfinder.intel.com/) e use este número para localizar mais informações sobre o processador e se ele suporta Enhanced Intel SpeedStep Technology.

EIST é uma tecnologia estabelecida. Você não deve ter um motivo para desligar EIST. No entanto, se você decidir que não deseja usar esse recurso, abra um chamado com a Equipe de suporte para desativar esse recurso.  Para desativar esse recurso, o servidor será reinicializado.
