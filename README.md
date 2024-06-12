Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.

1) Creo due componenti AppHeader e AppMain;

2) Aggiungo ad AppMain due sottocomponenti MainSelect e MainCardsList, che a sua volta avrà un altro sottocomponente MainCard.
   
Al caricamento della pagina, effettuate una chiama ajax all'API di Yu Gi Oh: https://db.ygoprodeck.com/api/v7/cardinfo.php e con i dati restituiti, stampate una card per ogni carta.

3) Creo una funizione get nel componente AppMain in cui avrò una chiamata all'API di Yu Gi Oh;

4) Creo un file store;

5) importo store nel componente MainCard;

6) faccio lo stesso con un parent in questo caso AppMain;

7) nel componente MainCard creo un ciclo v-for in cui metterò i dati delle carte;