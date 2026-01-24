# Progetto: Dashboard Web "Live Sports Results"
## Documentazione Tecnica e Funzionale

---

## 1. Panoramica del Progetto

### 1.1 Obiettivo

Realizzare un'applicazione web che mostri risultati sportivi e informazioni sugli eventi per il calcio europeo, utilizzando un feed di dati sportivi fornito dall'ESPN API. L'applicazione consente agli utenti di visualizzare i risultati delle partite, le partite in programma e lo stato degli eventi per i principali campionati di calcio europei.

L'obiettivo didattico del progetto è dimostrare la capacità di integrare API REST esterne, gestire e normalizzare dati in formato JSON, progettare un'architettura web client–server e documentare correttamente un progetto software. Attraverso questo progetto, lo studente acquisisce competenze pratiche nello sviluppo di applicazioni web complete, dalla gestione delle richieste HTTP lato client fino all'elaborazione dei dati lato server.

### 1.2 Descrizione Generale

L'applicazione "Live Sports Results" è una dashboard web che aggrega e visualizza informazioni relative agli eventi calcistici dei quattro principali campionati europei: Premier League (Inghilterra), La Liga (Spagna), Bundesliga (Germania) e Ligue 1 (Francia). L'interfaccia utente presenta i dati in modo chiaro e intuitivo, permettendo agli utenti di consultare rapidamente i risultati delle partite, verificare lo stato degli eventi e consultare le partite programmate per la giornata.

Il sistema è progettato seguendo un'architettura client–server moderna, dove il backend gestisce le comunicazioni con l'API esterna, elabora i dati ricevuti e li espone tramite endpoint REST dedicati. Il frontend, accessibile tramite browser web, consuma questi endpoint e aggiorna dinamicamente l'interfaccia utente senza necessità di ricaricare la pagina.

---

## 2. Analisi delle API

### 2.1 ESPN API

ESPN API è un servizio che fornisce dati sportivi completi tramite interfaccia REST, offrendo informazioni dettagliate su eventi sportivi, risultati delle partite, stati degli eventi e classifiche per numerosi sport e campionati a livello globale. L'API è particolarmente apprezzata per la sua affidabilità e la vastità dei dati coperti, rendendola una scelta ideale per applicazioni che necessitano di informazioni sportive aggiornate in tempo reale.

Per questo progetto, l'API viene utilizzata per ottenere dati relativi alle partite di calcio dei principali campionati europei, inclusi informazioni come squadre partecipanti, punteggi finali e parziali, orari di inizio, stati degli eventi e statistiche correlate. I dati sono restituiti in formato JSON, un formato standard per lo scambio di dati nelle applicazioni web moderne, che facilita l'elaborazione e la manipolazione lato client e server.

### 2.2 Campionati Supportati da ESPN

L'applicazione è stata progettata per visualizzare i risultati e le informazioni relative ai seguenti campionati di calcio europei, scelti per la loro rilevanza a livello internazionale e per la copertura mediatica di cui godono.

**Premier League (Campionato Inglese)**: Il campionato di calcio inglese, considerato uno dei più competitivi e seguiti al mondo, ospita club storici come Manchester United, Liverpool, Arsenal, Chelsea e Manchester City. L'API fornisce dati completi sulle partite, inclusi risultati in tempo reale per le partite in corso e archivio storico per quelle concluse.

**La Liga (Campionato Spagnolo)**: Il campionato spagnolo, dominato storicamente da club come Real Madrid, Barcellona e Atlético Madrid, offre partite di alto livello tecnico. L'integrazione con l'API permette di visualizzare tutti gli incontri del campionato con aggiornamenti sullo stato e sui risultati.

**Bundesliga (Campionato Tedesco)**: Il campionato tedesco, noto per il suo ritmo di gioco elevato e per la filosofia di sviluppo dei giovani talenti, include club come Bayern Monaco, Borussia Dortmund e RB Leipzig. L'applicazione mostra i risultati e le informazioni relative a tutte le partite del campionato.

**Ligue 1 (Campionato Francese)**: Il campionato francese, negli ultimi anni caratterizzato dalla presenza di star internazionali Paris Saint-Germain, fornisce dati sulle partite che vengono integrati nell'applicazione per offrire una panoramica completa del calcio europeo.



### 2.3 Flashscore API

Flashscore API è un servizio che fornisce dati sportivi tramite interfaccia REST, consentendo l’accesso a informazioni aggiornate su eventi sportivi, con particolare riferimento alle competizioni calcistiche. L’API permette di ottenere dati relativi a partite, risultati, stati degli incontri, calendari e statistiche associate ai campionati, risultando adatta allo sviluppo di applicazioni orientate alla consultazione di dati sportivi.

Nel contesto di questo progetto, l’API Flashscore viene utilizzata per cercare di ricavare informazioni relative ai marcatori dei principali campionati di calcio europei. Anche i dati di FLASHSCORE sono restituiti in formato JSON, uno standard ampiamente utilizzato nelle applicazioni web moderne, che facilita l’elaborazione e l’integrazione delle informazioni sia lato client che lato server.

---

## 3. Requisiti Funzionali

### 3.1 Visualizzazione Risultati

L'applicazione deve consentire la visualizzazione dei risultati delle partite per ciascuno dei quattro campionati supportati. Per ogni partita devono essere mostrate le squadre partecipanti, il punteggio finale (ove disponibile) e lo stato dell'evento. Gli stati possibili includono partite concluse (con risultato finale), partite in corso (con punteggio aggiornato in tempo reale) e partite programmate (con data e ora dell'incontro).

La visualizzazione deve essere organizzata in modo logico, raggruppando le partite per campionato e ordinandole cronologicamente. L'utente deve poter identificare immediatamente quale partita appartiene a quale campionato, visualizzando anche informazioni secondarie come il giorno e l'orario di gioco.

### 3.2 Gestione Eventi Giornalieri

L'applicazione deve presentare un elenco degli eventi sportivi della giornata corrente, mostrando per ciascun evento le squadre partecipanti, la data e l'orario dell'incontro, il campionato di riferimento e lo stato corrente dell'evento. Questa funzionalità permette agli utenti di avere una visione immediata del calendario giornaliero, facilitando il seguito delle partite di interesse.

La sezione dedicata agli eventi giornalieri deve aggiornarsi dinamicamente per riflettere lo stato corrente delle partite, distinguendo tra partite concluse (con relativo punteggio), partite in corso (con indicazione del tempo o dei minuti trascorsi) e partite future (con orario di inizio programmato).

### 3.3 Dettaglio Evento

Per ogni partita visualizzata, l'applicazione deve offrire la possibilità di accedere a informazioni dettagliate sull'evento. Il dettaglio dell'evento deve includere il risultato finale o parziale, lo stato corrente dell'evento (programmato, in corso, concluso, sospeso), la data e l'ora effettiva di svolgimento, e ulteriori informazioni contestuali come il numero di giornata del campionato.

La schermata di dettaglio deve presentare i dati in modo strutturato e leggibile, utilizzando formattazione appropriata per distinguere chiaramente le diverse informazioni e rendere l'esperienza utente quanto più intuitiva possibile.

### 3.4 Sistema di Filtri

L'applicazione deve implementare un sistema di filtri che consenta agli utenti di personalizzare la visualizzazione dei dati secondo criteri specifici. I filtri disponibili devono includere la selezione del campionato, permettendo di visualizzare esclusivamente le partite di Premier League, La Liga, Bundesliga o Ligue 1, oppure di combinare più campionati in una singola visualizzazione.

Il filtro temporale deve consentire la visualizzazione degli eventi recenti, delle partite della giornata corrente e degli eventi programmati per i giorni successivi. Questa funzionalità è essenziale per permettere agli utenti di navigare agevolmente tra le diverse partite senza dover scorrere manualmente liste troppo lunghe di informazioni.

---

## 4. Architettura del Sistema

### 4.1 Panoramica Architetturale

L'applicazione "Live Sports Results" adotta un'architettura client–server a tre livelli, progettata per garantire scalabilità, manutenibilità e separazione delle responsabilità. Il backend è responsabile della comunicazione con l'API ESPN esterna, della gestione sicura delle credenziali API, della normalizzazione dei dati ricevuti e dell'esposizione di endpoint REST verso il frontend. Il frontend è un'applicazione web accessibile tramite browser che consuma questi endpoint, aggiorna dinamicamente i dati tramite Fetch API e presenta un'interfaccia utente responsiva e intuitiva.

La comunicazione tra client e server avviene tramite il protocollo HTTP, utilizzando i metodi GET per il recupero dei dati. I dati vengono scambiati in formato JSON, un formato standard che facilita l'elaborazione sia lato server che lato client. L'architettura prevede inoltre un meccanismo di caching lato server per ottimizzare le richieste all'API esterna e ridurre la latenza percepita dall'utente finale.

### 4.2 Backend

Il componente backend dell'applicazione è sviluppato utilizzando tecnologie server-side che consentono la creazione di API REST robuste e performanti. Il server è responsabile di numerose funzioni critiche per il corretto funzionamento dell'applicazione, tra cui l'esecuzione delle richieste HTTP verso l'API ESPN, la gestione delle chiavi API in modo sicuro (evitando l'esposizione di credenziali sensibili nel codice client), la normalizzazione e il filtraggio dei dati ricevuti per adattarli alle esigenze specifiche dell'applicazione.

Il backend espone una serie di endpoint REST che il frontend utilizza per recuperare i dati necessari. Questi endpoint sono progettati seguendo le best practice delle API REST, utilizzando URL significativi, verbi HTTP appropriati e codici di stato HTTP standard per comunicare l'esito delle operazioni.

### 4.3 Endpoint del Backend

Gli endpoint esposti dal backend sono stati progettati per fornire al frontend tutti i dati necessari per le funzionalità dell'applicazione. Di seguito sono descritti gli endpoint principali con le relative funzionalità.

**Endpoint per i Risultati odierni**: L'endpoint `/api/scores/today` restituisce i risultati delle partite del giorno corrente per tutti i campionati supportati. Questo endpoint è ottimizzato per fornire una risposta rapida e include solo le partite effettivamente in programma per la giornata, riducendo il volume di dati trasferiti.

**Endpoint per campionato specifico**: L'applicazione espone endpoint dedicati per ciascun campionato supportato, consentendo al frontend di recuperare dati specifici senza dover filtrare lato client. Gli endpoint disponibili sono `/api/scores/premier-league` per il campionato inglese, `/api/scores/la-liga` per il campionato spagnolo, `/api/scores/bundesliga` per il campionato tedesco e `/api/scores/ligue-1` per il campionato francese. Ciascuno di questi endpoint restituisce i dati relativi alle partite del rispettivo campionato, incluse partite concluse, in corso e programmate.

**Endpoint per la lista dei campionati**: L'endpoint `/api/sports` (o `/api/leagues`) fornisce la lista dei campionati supportati dall'applicazione, insieme a informazioni aggiuntive come il nome completo del campionato, la nazione di appartenenza e eventuali logo o identificatori. Questo endpoint è utilizzato per popolare i filtri dell'interfaccia utente e per consentire la navigazione tra i diversi campionati.

### 4.4 Frontend

Il componente frontend dell'applicazione è sviluppato come applicazione web accessibile tramite qualsiasi browser moderno. L'interfaccia utente è costruita utilizzando HTML5 per la struttura, CSS per la presentazione visiva e JavaScript per la logica di interazione e il recupero dati asincroni.

Il frontend utilizza la Fetch API per eseguire richieste HTTP verso gli endpoint del backend, permettendo l'aggiornamento dinamico dei dati senza necessità di ricaricare la pagina. Questa caratteristica è fondamentale per fornire un'esperienza utente fluida e reattiva, specialmente durante l'aggiornamento dei punteggi in tempo reale per le partite in corso.

L'interfaccia è progettata per essere semplice e intuitiva, con una struttura a schede o sezioni che permette agli utenti di navigare facilmente tra i diversi campionati e filtrare i dati secondo le proprie preferenze. Il design responsive garantisce che l'applicazione sia utilizzabile su dispositivi con dimensioni di schermo diverse, inclusi smartphone, tablet e desktop.

---

## API utilizzata: ESPN API e FLASHSCORE

**ESPN API** e **FLASHSCORE** sono un servizio che fornisce dati sportivi tramite **API REST**.

L’API mette a disposizione informazioni quali:
- eventi sportivi programmati e recenti;
- risultati delle partite (scores);
- stato degli eventi (in corso, programmati, conclusi);
- supporto a diversi sport e campionati (Serie A, Premier League, NBA, NFL, ecc.);
- FLASHSCORE rispetto a ESPN fornisce anche i dati sui marcatori del campionato della liga.

**Java con Spring Boot**: Un framework enterprise che semplifica la configurazione e lo sviluppo di applicazioni Java, particolarmente adatto per progetti che richiedono robustezza, scalabilità e manutenibilità a lungo termine.

**Python con Flask o FastAPI**: Microframework Python che permettono la creazione rapida di API REST. FastAPI, in particolare, offre caratteristiche avanzate come la validazione automatica dei dati, la documentazione interattiva e alte prestazioni.

### 5.3 Strumenti di Sviluppo e Infrastruttura

**Controllo di versione**: Il progetto utilizza Git come sistema di controllo di versione distribuito, permettendo il tracciamento delle modifiche, la gestione dei branch per lo sviluppo parallelo e la collaborazione tra sviluppatori. Una piattaforma di hosting come GitHub, GitLab o Bitbucket può essere utilizzata per memorizzare il repository remoto e facilitare la collaborazione.

**Formato dati**: Il formato JSON (JavaScript Object Notation) è utilizzato per lo scambio di dati tra backend e frontend, nonché per la comunicazione con l'API ESPN esterna. JSON è il formato standard per le API REST moderne grazie alla sua leggibilità, compattezza e facilità di parsing.

**Ambiente di sviluppo**: L'ambiente di sviluppo consigliato include un editor di codice moderno come Visual Studio Code, che offre supporto nativo per JavaScript, HTML, CSS e numerose estensioni per lo sviluppo web. Per il backend, l'ambiente di sviluppo può includere l'IDE preferito in base alla tecnologia scelta (Visual Studio per ASP.NET Core, IntelliJ IDEA per Java, ecc.).

---

## 6. Flusso di Dati

### 6.1 Ciclo di Vita di una Richiesta

Il flusso di dati nell'applicazione "Live Sports Results" segue un percorso ben definito che inizia con la richiesta dell'utente e termina con la visualizzazione dei risultati aggiornati nell'interfaccia. Comprendere questo flusso è essenziale per garantire il corretto funzionamento dell'applicazione e per facilitare le operazioni di debugging e ottimizzazione.

Quando l'utente accede alla pagina web, il browser carica l'HTML, il CSS e il JavaScript necessari per l'esecuzione dell'applicazione. Durante questa fase iniziale, il JavaScript può eseguire chiamate asincrone verso il backend per recuperare i dati iniziali, come la lista dei campionati disponibili e le partite del giorno corrente. Queste richieste vengono gestite dalla Fetch API, che permette di eseguire operazioni di rete non bloccanti.

Il server backend riceve le richieste provenienti dal frontend e le elabora. Per ogni richiesta, il server verifica i parametri, costruisce la chiamata appropriata verso l'API ESPN (inserendo la chiave API negli header o nei parametri richiesti), attende la risposta e processa i dati ricevuti. La risposta dell'API ESPN, tipicamente in formato JSON, viene analizzata, filtrata e normalizzata secondo le esigenze dell'applicazione, quindi convertita in una risposta HTTP strutturata che viene inviata al client.

Il frontend riceve la risposta del backend, tipicamente un oggetto JSON contenente i dati richiesti, e la elabora per aggiornare l'interfaccia utente. Il JavaScript parsinga i dati, costruisce gli elementi HTML necessari (tabelle, schede, liste) e li inserisce nel DOM della pagina. L'utente visualizza così i dati aggiornati senza necessità di ricaricare la pagina.

### 6.2 Aggiornamento dei Dati

L'applicazione implementa meccanismi di aggiornamento automatico per garantire che le informazioni visualizzate siano sempre aggiornate, particolarmente importante per le partite in corso dove i punteggi cambiano in tempo reale. Due sono le strategie principali implementabili per mantenere sincronizzati i dati con la fonte originale.

La prima strategia prevede l'utilizzo del polling periodico, dove il JavaScript esegue richieste periodiche verso il backend a intervalli regolari (ad esempio ogni 30-60 secondi). Questa strategia è semplice da implementare e funziona in modo affidabile nella maggior parte dei casi, anche se può generare un numero elevato di richieste anche quando i dati non sono cambiati.

La seconda strategia, più avanzata, prevede l'utilizzo di WebSocket per stabilire una connessione bidirezionale tra client e server, permettendo al server di inviare aggiornamenti al client non appena disponibili. Questa strategia riduce la latenza degli aggiornamenti e ottimizza il traffico di rete, ma richiede un'implementazione più complessa e supporto specifico lato server.

Per questo progetto didattico, l'implementazione del polling periodico rappresenta un buon compromesso tra semplicità implementativa e funzionalità, consentendo di dimostrare la gestione delle operazioni asincrone e la manipolazione del DOM in risposta ai dati ricevuti.

---

## 7. Gestione degli Errori

### 7.1 Tipologie di Errori

Un'applicazione web che dipende da servizi esterni deve gestire correttamente diverse tipologie di errori che possono verificarsi durante il ciclo di vita delle richieste. Una gestione robusta degli errori migliora l'esperienza utente e facilita le operazioni di debugging e manutenzione.

Gli errori di rete possono verificarsi per problemi di connettività, timeout delle richieste o indisponibilità temporanea del server. Questi errori vengono tipicamente rilevati dalla Fetch API e devono essere gestiti mostrando un messaggio appropriato all'utente e, dove possibile, ritentando automaticamente la richiesta dopo un intervallo di tempo.

Gli errori lato server possono includere risposte con codici di stato HTTP che indicano problemi server (500 Internal Server Error) o risorse non trovate (404 Not Found). Il backend deve implementare una gestione centralizzata degli errori che garantisca risposte coerenti e informative anche in caso di eccezioni non previste.

Gli errori di autenticazione con l'API ESPN possono verificarsi se la chiave API non è valida, è scaduta o ha superato i limiti di utilizzo. Questi errori devono essere rilevati e comunicati agli sviluppatori per consentire l'aggiornamento delle credenziali, mentre all'utente deve essere mostrato un messaggio che spieghi l'indisponibilità temporanea del servizio.

### 7.2 Strategie di Gestione

L'applicazione implementa diverse strategie per gestire gli errori in modo efficace e minimizzare l'impatto sull'esperienza utente. A livello di frontend, tutte le richieste HTTP sono racchiuse in blocchi try-catch che intercettano le eccezioni e le gestiscono mostrando messaggi informativi nell'interfaccia. L'utente viene informato quando si verificano problemi nel recupero dei dati, con suggerimenti su come procedere (ad esempio, ritentare manualmente o controllare la connessione di rete).

A livello di backend, viene implementato un sistema di logging che registra gli errori con sufficiente dettaglio per facilitare il debugging, includendo timestamp, endpoint coinvolti, parametri della richiesta e dettagli dell'errore. I log possono essere scritti su file, console o sistemi di logging dedicati a seconda dell'ambiente di deployment.

La funzionalità di retry automatico può essere implementata per gestire errori transitori come problemi di rete temporanei. Il backend o il frontend possono ritentare automaticamente le richieste fallite un numero limitato di volte con intervalli crescenti, aumentando le probabilità di successo senza sovraccaricare il server in caso di problemi persistenti.

---

## 8. Considerazioni sulla Sicurezza

### 8.1 Gestione delle Credenziali API

La sicurezza delle credenziali API è un aspetto critico nello sviluppo dell'applicazione. La chiave API fornita da ESPN per l'accesso ai dati sportivi deve essere protetta da esposizione non autorizzata, poiché la compromissione potrebbe portare ad utilizzo non autorizzato delle quote, esaurimento dei limiti di chiamata o revoca dell'accesso.

L'approccio corretto prevede che la chiave API sia memorizzata esclusivamente lato server, in un file di configurazione o in variabili d'ambiente che non vengono mai esposte al client. Il frontend non deve mai contenere la chiave API in chiaro nel codice JavaScript, poiché qualsiasi utente potrebbe ispezionare il codice sorgente e recuperarla. Tutte le richieste verso l'API ESPN devono essere effettuate esclusivamente dal backend, che aggiunge la chiave API negli header di richiesta appropriati prima di inoltrarla al servizio esterno.

### 8.2 Protezione degli Endpoint

Gli endpoint esposti dal backend devono essere protetti da accessi non autorizzati e da utilizzo eccessivo. Sebbene per un progetto didattico le misure di sicurezza avanzate possono essere ridotte, è buona pratica implementare almeno una validazione dei parametri di input per prevenire attacchi di tipo injection e una limitazione della frequenza delle richieste (rate limiting) per evitare abusi.

La comunicazione tra frontend e backend dovrebbe avvenire preferibilmente tramite protocollo HTTPS, che garantisce la cifratura dei dati in transito e previene attacchi man-in-the-middle. In un ambiente di produzione, l'implementazione di meccanismi di autenticazione (come token JWT) può essere considerata se l'applicazione richiede utenti registrati o funzionalità personalizzate.

---

### Funzionalità implementate
- Modalità chiaro - scuro;
- Implementazione di ulteriori campionati calcistici;
- Aggiunta delle classifiche dei campionati implementati;
- Statistiche della squadra;
- Filtro per la selezione del campionato;
- Classifica marcatori LaLiga

### Funzionalità non implementate
- A causa di alcune limitazioni riscontrate durante la progettazione e l’utilizzo dell’API Flashscore, non è stato possibile implementare il recupero dei dati dei marcatori per tutti i campionati.
In particolare, l’API consente di ottenere i dati dei marcatori di questa stagione solamente per il campionato della LaLiga, mentre non fornisce tali informazioni per gli altri campionati.

---

## Conclusione
Il progetto web “Live Sports Results”, basato su **The Odds API**, permette di sviluppare una dashboard per la visualizzazione dei risultati sportivi, applicando competenze fondamentali di sviluppo web, integrazione di API REST esterne e progettazione di un’architettura client–server in un contesto realistico e didatticamente efficace.
