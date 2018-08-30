---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Nome e local do daemon de monitoramento do RAID
O {{site.data.keyword.cloud}} usa principalmente as placas RAID Adaptec e LSI, com algumas exceções para hardware
anterior. A tabela a seguir descreve os locais do gerenciador RAID, os locais do monitor, as definições e as
configurações de alerta RAID.

É possível configurar alertas RAID para que ignorem o processo de monitoramento do portal mudando o destino do servidor SMTP
e do e-mail de notificação na configuração para uma placa RAID. Se você mudar essas configurações, a IBM não poderá
notificá-lo sobre problemas do RAID nem controlar automaticamente o problema até a resolução. Não altere a configuração fornecida, a menos que você esteja ciente dos riscos.

<caption>Tabela 1. Configurações e configurações do RAID</caption>

||LSI Linux|Janelas LSI|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**Nome do gerenciador**|Gerenciador de armazenamento MegaRAID de LSI|Gerenciador de armazenamento MegaRAID de LSI|Gerenciador de armazenamento Adaptec|Gerenciador de armazenamento Adaptec|
|**Local do gerenciador**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nome do monitor**|MR_Monitor|MRMonitor|Gerenciador de eventos Adaptec|Gerenciador de eventos Adaptec|
|**Local do monitor**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nome do processo**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Local do log**|Local do log de mensagens padrão para o S.O., como /var/log/messages|Somente GUI|/usr/StorMan/RaidEvtA.log|Somente GUI|
|**Destino do e-mail de notificação**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Formato de origem do e-mail de notificação**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**Porta de e-mail**|25|25|25|25|
|**Servidor SMTP**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Opções de notificação alternativas**|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisa de configurações de firewall apropriadas.|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisa de configurações de firewall apropriadas.|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisa de configurações de firewall apropriadas.|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisa de configurações de firewall apropriadas.|
