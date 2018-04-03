---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introdução aos {{site.data.keyword.baremetal_short}}

Os {{site.data.keyword.baremetal_long}} fornecem a você desempenho e controle. Os {{site.data.keyword.baremetal_short}} não são executados em um hypervisor e você obtém acesso de baixo nível para os recursos de hardware. Além disso, nenhum outro cliente compartilhará o servidor com você -- é todo seu!
{:shortdesc}

Ao criar os {{site.data.keyword.baremetal_short}}, é possível customizar as especificações dos processadores e região para o sistema operacional e disco rígido.

Para provisionar os {{site.data.keyword.baremetal_short}}:
  1. Acesse **Cálculo > {{site.data.keyword.baremetal_short}}** e clique em **Incluir**.
  2. Selecione o local em que você deseja que a instância dos {{site.data.keyword.baremetal_short}} seja provisionada. Este é um data center em uma das regiões do {{site.data.keyword.Bluemix}}.
  3. Selecione a configuração para os servidores. Essa configuração se aplica a todos os servidores criados para esta instância.
  4. Selecione o número de servidores que você deseja que sejam criados para esta instância. Para cada servidor, insira um nome de host exclusivo.
  5. **Opcional:** insira uma URL em um arquivo de script ou texto que você definiu para configurar o servidor. O script de fornecimento deve usar um protocolo HTTPS. O script será transferido por download e executado após a instância ser provisionada, se possível. Se a URL não estiver associada a um script executável, o script simplesmente será transferido por download.
  6. Selecione o sistema operacional para os servidores. Esse sistema operacional se aplica a todos os servidores criados para esta instância.

Em uma hora, seus {{site.data.keyword.baremetal_short}} são provisionados e estão disponíveis para uso.
