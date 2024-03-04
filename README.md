- Descrizione:
  Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
  Al caricamento della pagina, effettuate una chiama axios all'API di Yu Gi Oh:
  (vi sconsigliamo di usare questo endpoint)
  https://db.ygoprodeck.com/api/v7/cardinfo.php
  e con i dati restituiti, stampate una card per ogni carta.
  
- ATTENZIONE:
  l’api restituisce tutti i risultati in un colpo solo. Per evitare attese e/o rallentamenti nelle richieste, potete diminuire il numero di risultati sfruttando i parametri *num* e *offset*
  https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0
  (endpoint consigliato)
  
- Bonus:
  Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.
