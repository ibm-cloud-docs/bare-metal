---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Informações de chamado de suporte do RAID
{:# bm-raid-support-ticket}

Se você tiver um problema ou pergunta sobre o uso do RAID em seu servidor bare
metal, poderá encontrar uma resposta no fórum do
[IBM developerWorks dW
Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} .Também é possível abrir um chamado de suporte. Para
obter informações sobre chamados de suporte, consulte
[Abrindo
um chamado de suporte.](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> Quando
um chamado de suporte é criado, você precisa fornecer os arquivos de log do RAID. As
informações nos arquivos de log do RAID são críticas para a recuperação de uma
configuração do RAID perdida. Fornecer os arquivos de log ajuda a equipe de suporte a
identificar a ordem da unidade, a associação da matriz, a geometria da matriz e os
problemas de cabeamento. Dependendo do tipo de controlador RAID que você está usando,
Adaptec ou LSI, use os comandos a seguir para obter os arquivos de log do RAID.

**Nota:** Conceder permissão para a
reinicialização/desligamento da atualização inicial ou solicitar que a unidade seja hot swap acelera o processo de chamado de suporte, .

<b>Placas RAID Adaptec</b><br>
Use o comando a seguir para obter os arquivos de log para placas Adaptec RAID. Certifique-se
de incluir a saída completa desse arquivo de log em seu chamado de suporte.

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>Placas RAID LSI</b><br> Use os comandos a seguir para obter os arquivos de log para placas RAID LSI. É necessário incluir a saída completa desses arquivos de log em seu chamado de suporte.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**Importante:** certifique-se de fazer backup de qualquer trabalho
antes do início da resolução de problemas.
