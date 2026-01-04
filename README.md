# Progetto: Dashboard “Live Sports Results”

## Obiettivo
Realizzare un’applicazione (web o mobile) che mostri **risultati sportivi in tempo reale** per diversi sport (calcio, basket, tennis, ecc.), utilizzando un **feed di dati sportivi** come quelli forniti da **Oddspedia Data Feeds** o servizi equivalenti.

L’obiettivo didattico è dimostrare la capacità di:
- integrare API esterne,
- gestire dati dinamici,
- progettare un’architettura client–server,
- documentare correttamente un progetto software.

---

## API utilizzata: Oddspedia Data Feeds

Oddspedia mette a disposizione **feed sportivi** che forniscono:
- partite programmate (fixture),
- risultati in tempo reale (live scores),
- stato delle partite (non iniziata, in corso, terminata),
- sport multipli (calcio, basket, tennis, hockey, volley, eSports).

I dati sono generalmente forniti in **formato JSON**, ideali per essere consumati da applicazioni software.

> Nota: Oddspedia fornisce anche widget pronti, ma per il progetto l’interesse è l’utilizzo dei **feed dati**, previa registrazione gratuita.

---

## Funzionalità principali dell’applicazione

### 1. Live Scores
- Visualizzazione dei risultati in tempo reale
- Aggiornamento automatico senza ricaricare la pagina

### 2. Calendario Partite
- Elenco delle partite giornaliere
- Informazioni base: squadre, data, ora, sport

### 3. Dettaglio Partita
- Punteggio aggiornato
- Stato dell’incontro (live / conclusa)
- Eventuali statistiche disponibili

### 4. Filtri
- Filtro per sport
- Filtro per competizione o lega

### 5. Funzionalità opzionali
- Visualizzazione quote
- Storico risultati
- Evidenziazione eventi importanti (gol, set, fine match)

---

## Architettura del sistema

### Backend
- Applicazione server (Java, C#, Node.js, Python)
- Responsabile delle chiamate all’API Oddspedia
- Normalizzazione dei dati ricevuti
- Esposizione di endpoint REST verso il frontend

Esempio di endpoint interno:
