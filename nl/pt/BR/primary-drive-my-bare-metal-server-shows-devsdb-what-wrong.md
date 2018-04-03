---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A unidade primária no meu servidor bare metal aparece como /dev/sdb. O que está errado?

Isso pode ser causado pelo Disco virtual do IPMI ocupar o slot /dev/sda. Isso pode ser desativado com segurança conectando ao IPMIView e navegando até a guia Mídia virtual. Selecione **Opções> Desativar** e clique no botão **Aplicar** para fazer a mudança. Quando o servidor bare metal for reinicializado em seguida, a unidade primária exibirá /dev/sda.
