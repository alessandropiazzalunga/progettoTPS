# Progetto: Dashboard Web “Live Sports Results”

## Obiettivo
Realizzare un’**applicazione web** che mostri **risultati sportivi** e informazioni sulle competizioni per diversi sport (calcio, basket, tennis, ecc.), utilizzando un **feed di dati sportivi** fornito da **TheSportsDB API**.

L’obiettivo didattico del progetto è dimostrare la capacità di:
- integrare API REST esterne;
- gestire e normalizzare dati in formato JSON;
- progettare un’architettura web client–server;
- documentare correttamente un progetto software.

---

## API utilizzata: TheSportsDB

**TheSportsDB** è un servizio che fornisce dati sportivi tramite **API REST**, accessibili previa registrazione e utilizzo di una **chiave API gratuita**.

L’API mette a disposizione informazioni quali:
- eventi sportivi (passati, futuri e in corso);
- risultati delle partite;
- campionati e competizioni;
- squadre e giocatori;
- supporto a sport multipli (calcio, basket, tennis, hockey, motorsport, ecc.).

I dati sono restituiti in **formato JSON**, ideali per essere consumati da applicazioni web.

> **Nota:** TheSportsDB non fornisce dati di betting o quote live, ma una base dati sportiva completa, adatta a progetti didattici.

---

## Funzionalità principali dell’applicazione web

### 1. Risultati delle Partite
- Visualizzazione dei risultati delle partite concluse
- Visualizzazione delle partite in programma
- Indicazione dello stato dell’evento (scheduled / finished)

### 2. Calendario Eventi
- Elenco degli eventi sportivi giornalieri o settimanali
- Informazioni principali:
  - squadre partecipanti
  - data e ora
  - competizione
  - sport di riferimento

### 3. Dettaglio Evento
- Risultato finale o parziale
- Informazioni sull’evento (stadio, lega, stagione)
- Eventuali dettagli aggiuntivi disponibili tramite API

### 4. Filtri
- Filtro per sport
- Filtro per lega o campionato
- Filtro per data

### 5. Funzionalità opzionali
- Storico risultati per squadra o lega
- Visualizzazione informazioni sulle squadre (logo, città, anno di fondazione)
- Pagina di dettaglio squadra con ultimi eventi disputati
- Evidenziazione eventi recenti o imminenti

---

## Architettura del sistema

### Backend
- Applicazione server web
- Responsabile delle chiamate all’API **TheSportsDB**
- Gestione sicura della chiave API
- Normalizzazione e filtraggio dei dati ricevuti
- Esposizione di endpoint REST verso il frontend

Esempi di endpoint backend:
- `/api/events/today`
- `/api/events/league/{id}`
- `/api/team/{id}`
- `/api/sports`

### Frontend
- Applicazione web accessibile tramite browser
- Consumo degli endpoint REST del backend tramite HTTP
- Aggiornamento dinamico dei dati (AJAX / Fetch API)
- Interfaccia utente responsiva e intuitiva

---

## Tecnologie suggerite

### Frontend
- HTML5, CSS3, JavaScript
- Framework opzionali: React, Vue.js, Angular

### Backend
- Node.js (Express)
- ASP.NET Core
- Java Spring Boot
- Python Flask / FastAPI

### Altre tecnologie
- Formato dati: JSON
- Architettura: REST
- Versionamento: Git

---

## Conclusione
Il progetto web “Live Sports Results”, basato su **TheSportsDB**, consente di sviluppare una dashboard web per la consultazione di dati sportivi, applicando concetti fondamentali di sviluppo web, integrazione di API REST e architettura client–server.
