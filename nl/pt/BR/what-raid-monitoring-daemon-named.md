---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Nome e local do daemon de monitoramento do RAID
O {{site.data.keyword.cloud}} usa principalmente os cartões RAID Adaptec e LSI com algumas exceções para hardware anterior. O gráfico abaixo descreve os locais do gerenciador de RAID, os locais do monitor, configurações e configurações de alerta do RAID.

É possível configurar alertas do RAID para efetuar bypass do processo de monitoramento do portal, mudando o servidor SMTP e o destino de E-mail de notificação na configuração para um cartão RAID especificado. Quando essas configurações são mudadas, a IBM não pode notificá-lo sobre problemas do RAID ou rastrear automaticamente o problema até a resolução. Não altere a configuração fornecida, a menos que você esteja ciente dos riscos.

||LSI - Linux|LSI - Windows|Adaptec - Linux|Adaptec - Windows|
|---|---|---|---|---|
|**Nome do gerenciador**|Gerenciador de armazenamento MegaRAID de LSI|Gerenciador de armazenamento MegaRAID de LSI|Gerenciador de armazenamento Adaptec|Gerenciador de armazenamento Adaptec|
|**Local do gerenciador**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nome do monitor**|MR_Monitor|MRMonitor|Gerenciador de eventos Adaptec|Gerenciador de eventos Adaptec|
|**Local do monitor**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nome do processo**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Local do log**|Local do log de mensagens padrão para S.O., por exemplo /var/log/messages|Somente GUI|/usr/StorMan/RaidEvtA.log|Somente GUI|
|**Destino do e-mail de notificação**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Formato de origem do e-mail de notificação**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**Porta de e-mail**|25|25|25|25|
|**Servidor SMTP**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Opções de notificação alternativas**|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisará de configurações de firewall apropriadas.|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisará de configurações de firewall apropriadas.|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisará de configurações de firewall apropriadas.|Mudar o Servidor SMTP para um servidor SMTP local. O servidor SMTP local precisará de configurações de firewall apropriadas.|
