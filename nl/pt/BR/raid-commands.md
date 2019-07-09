---

copyright:
  years: 1994, 2019
lastupdated: "2018-07-10"

keywords: raid controller commands, raid commands

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# comandos do controlador RAID
{: #bm-raid-controller-commands}

Use o utilitário de linha de comandos do Adapatec para executar os comandos do controlador RAID.
A seguir estão os comandos do controlador RAID mais comuns que podem ser usados.
{:shortdesc}

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ lista o tipo de operação, o número da unidade lógica, o tamanho da unidade lógica e o progresso da
operação. Também é possível ver o status de quaisquer comandos em segundo plano que estejam em execução, como os seguintes itens:
<ul>
  <li> Reconstrução mais recente
  <li> Sincronização
  <li> Migração da Unidade Lógica
  <li> Compactação / expansão
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ lista as informações sobre os controladores, as unidades lógicas e as unidades físicas. É possível ver informações como os itens a seguir:
<ul>
  <li> Tipo de controlador
  <li> BIOS, bloqueio de inicialização, driver de dispositivo e versões de firmware 
  <li> Tipo de dispositivo físico, ID do dispositivo, presença do PFA 
  <li> Estado do dispositivo físico 
  <li> Informações de gabinete: ventilador, fonte de alimentação e temperatura
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b> _GETLOGS_ fornece
acesso aos logs de status e de eventos de um controlador. _DEVICE xxx_ exibe um log de quaisquer erros de
dispositivo encontrados pelo controlador.

Consulte o exemplo a seguir para a saída produzida usando o comando _GETLOGS_:
```
driveErrorEntry smartError .. ............................ falso 
vendorID ................................ WDC
serialNumber ............................ WD-XXX wwn ..................................... xxxxxxxxxxxxxxxx-ID do deviceID CC_FILTER ................................ 10 productID ............................... WD1003FB numParityErrors ......................... 0 linkFailures ............................ 0 hwErrors ................................ 0 abortedCmds ............................. 7 Média de Erros ............................ 20 smartWarning ............................ 0
```

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir” </code></b><br>
Use esse comando para mostrar as unidades específicas e quaisquer possíveis erros de unidade que possam existir.
O exemplo a seguir mostra a saída:
```
Unidade /c0/e252/s0-Informações Detalhadas: 
Contador de Escudos = 0 Contagem de erros de mídia = 0  Outra Contagem de Erros = 0 
Temperatura da Unidade = 24C (75,20 F) 
Contagem de Falhas Predictivas = 0  
Alerta S.M.A.R.T sinalizado pela unidade = Não 
SN = XXXX 
Revisão de Firmware = SN04   Unidade /c0/e252/s1-Informações Detalhadas: 
Contador de Escudos = 0 
Contagem de erros de mídia = 0  
Outra Contagem de Erros = 0 
Temperatura da unidade = 22 °C (71,60 °F) 
Contagem de Falhas Predictivas = 0  
Alerta S.M.A.R.T sinalizado pela unidade = Não 
SN = xxxx 
Revisão de Firmware = SN03 

Unidade /c0/e252/s2-Informações Detalhadas:  Contador de Escudos = 0 
Contagem de erros de mídia = 0  
Outra Contagem de Erros = 0 
Temperatura da unidade = 21º C (69,80º F)  Contagem de Falhas Predictivas = 0  
Alerta S.M.A.R.T sinalizado pela unidade = Não SN = xxxx 
Revisão de Firmware = SN04   Drive /c0/e252/s3 - Informações detalhadas:  Contador de Escudos = 0 
Contagem de erros de mídia = 0  Outra Contagem de Erros =  Temperatura da Unidade = 23C (73,40 F) 
Contagem de Falhas Predictivas = 0  Alerta S.M.A.R.T sinalizado pela unidade = Não 
SN = xxxx Revisão de firmware = SN03  
```

<!--<code><b>/opt/MegaRAID/storcli/storcli64 /c0 show all | less </code></b>-->
<!--You use this command to view RAID health, size, name, and other important information.-->

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild</code></b>
Esse comando exibe o status de reconstrução de todas as unidades e o tempo estimado para concluir a reconstrução. Você verá essa
saída ao executar o comando:
```
--------------------------------------------- Drive-ID Progress% Status Estimated Time Left 
--------------------------------------------- /c0/e252/s0 - Not in progress  /c0/e252/s1 - Not in progress  /c0/e252/s2-Não está em progresso  /c0/e252/s3-Não está em progresso --------------------------------------------- 
```

<b>Alerta "Spam" do RAID</b> Mude a seção "global" da configuração padrão
(/opt/lsi/mrmonitor/MegaMonitor/config-current.xml): 
```<global>
 <severity level="FATAL"> 
<do-systemlog/> 
< do-email/>  </severity> <severity level="CRITICAL"> 
< do-email/>  <do-systemlog/> 
< /severity>  < gravidade level="WARNING ">  <do-email/> 
<do-systemlog/> 
< /severity>  < gravidade level="INFO "> < do-systemlog/> < /severity>  </global> 
```
para este: 
```
<global> 
<severity level="FATAL"> 
<do-systemlog/> 
< do-email/>  </severity> 
<severity level="CRITICAL"> 
<do-email/> 
<do-systemlog/> 
</severity> 
<severity level="WARNING"> 
<do-systemlog/> 
</severity> 
< gravidade level="INFO "> < do-systemlog/>  </severity> 
</global> 
```
**Nota:** remova a tag "do-email" para o nível "WARNING". Como alternativa, mude o nível de segurança para "INFO".

## Erros comuns da unidade
{: #bm-common-drive-errors}

Os erros de driver mais comuns são os erros inteligentes, os erros de hardware e os erros de mídia. Você verá esses erros se
uma unidade estiver falhando. Assim, é necessário substituir a unidade o mais rapidamente possível.

Embora não sejam atípicos, os comandos interrompidos são outro erro comum. Mas, se os comandos interrompidos aumentarem em
número (como 100), um chamado de suporte deverá ser aberto.  

Os erros de link podem indicar que um cabo precisa ser reposicionado ou substituído.

### Informações do chamado de suporte
{: #bm-raid-support}

**Placas RAID Adaptec** <br> Certifique-se de incluir a saída completa de `arcconf getconfig 1/arcconf getlogs 1
device tabular` ao criar um chamado de suporte. Fornecer essas informações ajuda a equipe de suporte a identificar a ordem
da unidade, a associação da matriz, a geometria da matriz e os problemas de cabeamento. Essas informações são críticas para a recuperação de uma configuração RAID perdida. Para acelerar o processo de chamado de suporte, conceda permissão para a reinicialização/desligamento da atualização inicial ou
solicite que ela seja hot swap.

**Placas RAID LSI** <br> Use os comandos a seguir para obter os arquivos de log para placas RAID LSI. É necessário incluir a
saída completa desses arquivos de log com o chamado de suporte.
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Nota**: certifique-se de fazer backup de qualquer trabalho antes que a resolução de problemas seja feita.
