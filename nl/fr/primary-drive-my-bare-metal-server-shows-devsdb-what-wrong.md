---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# L'unité principale de mon serveur bare metal se présente sous la forme /dev/sdb. Que se passe-t-il ?

Cela peut être dû au fait que le disque virtuel d'IPMI utilise l'emplacement /dev/sda. Pour désactiver cette association, connectez-vous à IPMIView et accédez à l'onglet Virtual Media. Sélectionnez **Options > Disable**, puis cliquez sur le bouton **Apply** pour effectuer la modification. Au prochain redémarrage du serveur bare metal, /dev/sda apparaîtra comme unité principale.
