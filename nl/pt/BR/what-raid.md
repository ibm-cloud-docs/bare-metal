---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: raid, about raid

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Sobre RAID
{: #bm-raid-levels}

O RAID (Redundant Array of Independent Disks) cria um único disco de dados utilizáveis, em que vários discos físicos são combinados em uma matriz para melhor velocidade e tolerância a falhas. A seguir estão os três conceitos principais em RAID:
* **Espelhamento**: copiando dados para mais de um disco
* **Striping**: dividindo os dados em mais de um disco
* **Correção de erro** (tolerância a falhas): os dados redundantes são armazenados para permitir que os problemas sejam detectados e possivelmente corrigidos.

Embora existam muitos níveis diferentes de RAID, o {{site.data.keyword.IBM_notm}} escolhe suportar os tipos de RAID mais comuns: 0, 1, 5, 6 e 10. Os diferentes níveis do RAID usam uma ou mais das técnicas a seguir, dependendo dos requisitos do sistema. O principal propósito é usar RAID para melhorar a confiabilidade usando 3Ware 9550SX RAID SATA ou um controlador Adaptec SA-SCSI RAID para todas as soluções RAID implementadas.

O RAID não é uma solução de backup. Em vez disso, o RAID cria um único disco de dados utilizáveis, em que vários discos físicos são combinados em uma matriz para melhor velocidade e tolerância a falhas.
{: note}

**RAID 0** (Conjunto de faixas sem paridade / Matriz não redundante) Implementa a separação de dados em faixas, em que os blocos de arquivos são gravados em múltiplos discos em fragmentos que requerem no mínimo dois discos. A vantagem de um RAID 0 é que a velocidade de leitura/gravação é significativamente aumentada. Quanto mais discos estiverem na matriz, maior a largura da banda. A desvantagem para um RAID 0 é que ele não tem tolerância a falhas. Se uma única unidade falhar, a matriz será quebrada. Além disso, o RAID 0 não implementa a verificação de erros. Portanto, qualquer erro também é irrecuperável. Uma solução comum para a tolerância a falhas é ter uma unidade fora da matriz usada como armazenamento de backup em uma falha de hardware.

**RAID 1** (Conjunto espelhado sem paridade) Implementa o espelhamento de dados. Os dados são duplicados em 2 ou 4 discos por meio de um controlador RAID de hardware e fornecem alguma tolerância a falhas. A matriz será recuperável se pelo menos uma unidade não falhar. Ela fornecerá um desempenho de leitura mais rápido do que uma unidade única e redundância de unidade se uma falha ocorrer. A velocidade de gravação é ligeiramente reduzida.

**RAID 5** (Conjunto dividido com paridade distribuída dual) Implementa a separação de dados em faixas em um nível de bloco e distribui paridade entre os discos. As informações de paridade permitem a recuperação da falha de qualquer unidade única porque quaisquer leituras seguintes podem ser calculadas da paridade distribuída. O RAID 5 também permite o aumento de velocidades de leitura/gravação e permite o uso mais eficiente do espaço em disco. O RAID 5 requer um mínimo de três discos.

**RAID 6** (Paridade dupla) Implementa faixas de paridade dupla em cada disco e permite que dois discos falhem antes que quaisquer dados sejam perdidos. Como o RAID 6 tem uma capacidade de duas unidades de disco que são dedicadas ao armazenamento de dados de paridade em um conjunto de paridades, maiores operações de E/S ocorrem com RAID 6 do que com RAID 5. Essas operações de E/S maiores podem diminuir o desempenho. O RAID 6 requer no mínimo 4 discos e no máximo 18.

**RAID 10** (RAID 1 + 0) Cria múltiplos espelhos, em que os dados são organizados como faixas em múltiplos discos e, então, os conjuntos de discos divididos são espelhados. O RAID 10 oferece a mesma tolerância a falhas que o RAID 1 com o aumento de velocidades de leitura/gravação de mais de um volume RAID 1 único ou unidade única. O nível do RAID 10 requer quatro discos para implementação.
