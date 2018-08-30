---


copyright:

  years: 2016, 2018
lastupdated: "2018-04-02"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Gerenciando servidores bare metal
{: #managing}


É possível parar, iniciar, reiniciar e cancelar servidores.
{:shortdesc}

## Replicando uma instância do servidor
É possível copiar ou clonar uma instância do servidor bare metal para replicar a configuração do servidor e rapidamente ter um novo servidor funcionando.
{:shortdesc}

Para clonar a instância:
 1. Acesse o menu e selecione **Configurar réplica**. Todas as configurações são copiadas. Nenhum dado ou conteúdo é copiado.
 2. Insira um nome de servidor exclusivo.
 3. Especifique o nome de domínio.

## Recarregando o sistema operacional
Ocasionalmente, talvez você queira recarregar o sistema operacional no servidor.
{:shortdesc}

Para recarregar o sistema operacional:
 1. Faça backup de todos os dados antes de iniciar. Se essa etapa for ignorada, todos os dados existentes serão perdidos e
não poderão ser recuperados.
 2. Acesse o menu e selecione **Recarregamento de S.O.**. É possível selecionar uma dessas opções:
  * Mudar o sistema operacional para um diferente e recomeçar com novas configurações.
  * Manter o sistema operacional existente com as configurações atuais, mas apagar os dados do servidor para recomeçar.

Durante o recarregamento do S.O., o servidor ficará off-line e indisponível para uso. O tempo de recarregamento varia com base na capacidade do servidor e o sistema operacional. Se você definiu um script de provisão, todas as configurações serão restauradas após a conclusão do recarregamento. Se seus dados foram submetidos a backup antes do recarregamento do S.O., será possível fazer upload deles para o servidor quando ele estiver disponível.

## Excluindo a instância do servidor
A qualquer momento, é possível excluir a instância do Bare Metal Server caso você não precise mais dela e não queira ser
cobrado.
{:shortdesc}

Para excluir a instância, acesse o menu e selecione **Cancelar servidor**.

## Desligando um servidor
É possível criar um servidor antecipadamente para a preparação do uso. Depois de criar o servidor, desligue-o para assegurar
que nada seja mudado e que ninguém possa acessá-lo. Quando você estiver pronto, será possível ligar o servidor e deixá-lo pronto em questão de minutos.
{:shortdesc}

Para desligar o servidor, acesse o menu e selecione **Ligar/Desligar**. Enquanto o servidor estiver
desligado, você ainda será faturado.

**Nota:** se o servidor for desligado, ele permanecerá no estado desligado e você deverá
ligá-lo manualmente.
