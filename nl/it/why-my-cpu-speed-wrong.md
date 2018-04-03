---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Perché la velocità della CPU è errata?

Poniamo il caso che tu acceda a un server per controllare le informazioni sulla CPU e noti che la velocità dei processori non era corretta. Questa discrepanza può essere dovuta a EIST (Enhanced Intel SpeedStep Technology). EIST è il nome Intel per la tecnologia di ridimensionamento della frequenza dinamico.  Questa tecnologia è detta anche *Limitazione CPU* o *regolazione della risposta del bus* (bus slewing) nei sistemi meno recenti. Su alcuni sistemi AMD, ci sono delle tecnologie simili chiamate *Cool'N'Quiet* o *PowerNow!*.  Pur non essendo tutte uguali, queste tecnologie hanno lo stesso obiettivo, ossia ridurre il consumo energetico e la produzione di calore quando il processore non è utilizzato in modo intensivo rallentando la velocità della CPU. Quando il server è di nuovo sotto carico, aumentano la velocità di clock come necessario.

Se vuoi sapere se il processore Intel sul tuo server supporta SpeedStep, nel portale clienti: 
1. Fai clic su **Dispositivi**.
* Identifica il tuo server nell'elenco.
* Fai clic sul nome server per visualizzare i **Dettagli dispositivo**.
* Individua la sottosezione denominata **Hardware** per trovare il numero di modello della CPU del processore del server.
* Con il numero di modello del processore del server, vai a [Intel Processor Finder](http://processorfinder.intel.com/) e usa questo numero per trovare ulteriori informazioni sul processore e per sapere se supporta Enhanced Intel SpeedStep Technology.

EIST è una tecnologia consolidata. Non dovresti avere alcun motivo per disattivare EIST. Tuttavia, se decidi che non vuoi usare questa funzione, apri un ticket con il team di supporto per disabilitare questa funzione. La disabilitazione di questa funzione prevede il riavvio del server.
