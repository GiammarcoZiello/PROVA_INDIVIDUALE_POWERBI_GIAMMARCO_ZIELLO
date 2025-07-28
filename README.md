PROVA_FINALE_POWERBI
POWERBI Analisi Dataset OlistStore composto dalle seguenti tabelle: • olist_orders_dataset

• olist_order_items_dataset

• olist_order_payments_dataset

• olist_order_reviews_dataset

• olist_products_dataset

• olist_customers_dataset o olist_order_customer_dataset

• olist_sellers_dataset

• olist_geolocation_dataset

• traduzione_nome_categoria_prodotto


Le singole tabelle presentavano problemi relativi al formato dati e per la presenza di caratteri speciali che rendevano difficile la lettura della reportistica. Valori mancanti come data di consegna o spedizione mancanti in alcuni ordini, soprattutto quelli cancellati o mai spediti, valori inconsistenti, dati duplicati o ridondanti, assenza di una tabella "Calendario" e la lingua delle categorie prodotto (la quale si è preferita mantenere invariata). Dopo una prima pulizia dei dati e delle tabelle, andando a sistemare i vari errori e ad effettuare le varie sistemazioni di formato necessarie per l'analisi, ci si è soffermati sui vari livelli di analisi al fini di individuare le diverse colonne calcolate per tabelle ei possibili marge tra le stesse, necessari per la scrittura di DAX o per effettuare analisi particolari nonché per denormalizzare il dataset. Nella tabella Order_Items, la quale è stata mergiata con la tabella relativa alle Reviews, abbiamo provveduto a creare una colonna calcolata che ci fornisce, in modo visivo, le stelle relative al punteggio di ogni singolo ordine. Nella tabella Ordini abbiamo creato colonne calcolate necessarie per l'analisi relativa alle spedizioni dal nome:

• Fine settimana/giorni feriali: fornisce informazioni circa il giorno in cui è stato effettuato l'ordine.

• Stato_consegna: che indica se l'ordine è stato consegnato, se è puntuale o in ritardo.

• Giorni di consegna effettivi: Che ci fornisce informazioni circa i giorni effettivi per la consegna.

• Tipologia di consegna: Ci indica se la consegna, in base a giorni trascorsi per il completamento, è lenta, standard o espressa.


A seguito dell'analisi e della manipolazione dei dati abbiamo provvedo a caricare le tabelle su PowerBI ea disporre i vari collegamenti con le varie cardinalità delle tabelle principali necessarie per la nostra analisi. Abbiamo provveduto a creare una tabella “Calendario”

Abbiamo poi provveduto a creare le misure DAX necessarie per la nostra analisi utilizzando funzioni come DIVIDE, CALCULATE, COUNTROWS, AVERAGE, AVERAGEX, PARALLELPIOD, SAMEPERIODLASTYEAR.


Dopo la creazione delle prime DAX ci si è dedicati all'attività grafica e di reportistica andando a creare le diverse pagine: • Menù: Pagina interattiva con i singoli bottini per richiamare le singole pagine del report.

• Ordini: Pagina dedicata all'analisi degli ordini con la presenza di schede, KPI, grafici e bottoni filtro per un totale di 6 grafici.

• Ricavi: Pagina dedicata all'analisi dei ricavi con la presenza di schede, KPI, grafici e bottoni filtro per un totale di 6 grafici.

• Recensioni: Pagina dedicata all'analisi delle recensioni con la presenza di schede, KPI, grafici e bottoni filtro per un totale di 4 grafici.

• Pagamenti: Pagina dedicata all'analisi dei pagamenti con la presenza di schede, KPI, grafici e bottoni filtro per un totale di 5 grafici.

• Spedizioni: Pagina dedicata all'analisi delle spedizioni con la presenza di schede, KPI, grafici e bottoni filtro.

Tutte le pagine del report sono integrate con filtri, segnalibri e drill – through. Aspetti da modificare/implementare sono sicuramenti incentrati sulla necessità di procedere con un'analisi più dettagliata della sezione recensioni.
