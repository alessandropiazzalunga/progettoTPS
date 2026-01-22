# Progetto: Dashboard Web “Live Sports Results”

## Obiettivo
Realizzare un’**applicazione web** che mostri **risultati sportivi** e informazioni sugli eventi per diversi sport (calcio, basket, ecc.), utilizzando un **feed di dati sportivi** fornito da **ESPN API**.

L’obiettivo didattico del progetto è dimostrare la capacità di:
- integrare API REST esterne;
- gestire e normalizzare dati in formato JSON;
- progettare un’architettura web client–server;
- documentare correttamente un progetto software.

---

## API utilizzata: ESPN

**ESPN API** è un servizio che fornisce dati sportivi tramite **API REST**.

L’API mette a disposizione informazioni quali:
- eventi sportivi programmati e recenti;
- risultati delle partite (scores);
- stato degli eventi (in corso, programmati, conclusi);
- supporto a diversi sport e campionati (Serie A, Premier League, NBA, NFL, ecc.).

I dati sono restituiti in **formato JSON**, facilmente integrabili in applicazioni web.

> **Nota:** ESPN API è orientata principalmente al mondo delle scommesse sportive, ma fornisce anche endpoint dedicati ai **risultati**, utilizzabili per scopi didattici e informativi.

---

## Funzionalità principali dell’applicazione web

### 1. Risultati delle Partite
- Visualizzazione dei risultati delle partite recenti
- Visualizzazione delle partite in programma
- Indicazione dello stato dell’evento (in corso / terminato)

### 2. Eventi Giornalieri
- Elenco degli eventi sportivi della giornata corrente
- Informazioni principali:
  - squadre partecipanti
  - data e ora dell’incontro
  - sport e campionato di riferimento

### 3. Dettaglio Evento
- Risultato finale o parziale
- Stato dell’evento
- Data e ora di svolgimento

### 4. Filtri
- Filtro per sport
- Filtro per campionato (es. Serie A, NBA)
- Filtro temporale (eventi recenti)

### 5. Funzionalità opzionali
- Separazione dei risultati per campionato
- Evidenziazione delle partite in corso
- Aggiornamento automatico dei risultati

---

## Architettura del sistema

### Backend
- Applicazione server web
- Responsabile delle chiamate all’API **The Odds API**
- Gestione sicura della chiave API
- Normalizzazione e filtraggio dei dati ricevuti
- Esposizione di endpoint REST verso il frontend

Esempi di endpoint backend:
- `/api/scores/today`
- `/api/scores/seriea`
- `/api/scores/nba`
- `/api/sports`

### Frontend
- Applicazione web accessibile tramite browser
- Consumo degli endpoint REST del backend tramite HTTP
- Aggiornamento dinamico dei dati tramite Fetch API
- Interfaccia utente semplice e intuitiva

---

## Tecnologie suggerite

### Frontend
- HTML5
- JavaScript (Fetch API)

### Backend
- Node.js (Express)
- ASP.NET Core
- Java Spring Boot
- Python Flask / FastAPI

### Altre tecnologie
- Formato dati: JSON
- Architettura: REST
- Versionamento del codice: Git
- Ambiente di sviluppo: Visual Studio

---

## Conclusione
Il progetto web “Live Sports Results”, basato su **The Odds API**, permette di sviluppare una dashboard per la visualizzazione dei risultati sportivi, applicando competenze fondamentali di sviluppo web, integrazione di API REST esterne e progettazione di un’architettura client–server in un contesto realistico e didatticamente efficace.
