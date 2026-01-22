# 📊 Progetto: Dashboard Web “Live Sports Results”

## 🎯 Obiettivo
Realizzare un’**applicazione web** che mostri **risultati sportivi in tempo reale** e informazioni sugli eventi per diversi sport (calcio, basket, ecc.), utilizzando un **feed di dati sportivi** fornito da **ESPN API**.

Il progetto dimostra competenze in:
- integrazione di API REST esterne;
- gestione e normalizzazione di dati JSON;
- progettazione di un’architettura web client–server;
- documentazione tecnica;
- arricchimento dell’esperienza utente tramite **statistiche dettagliate delle squadre**.

---

##  API utilizzata: ESPN API
L’**ESPN API** fornisce dati sportivi tramite endpoint REST, tra cui:
- eventi sportivi programmati e recenti;
- risultati delle partite;
- stato degli eventi (live, programmati, conclusi);
- supporto a diversi sport e campionati (Serie A, Premier League, NBA, NFL, ecc.).

I dati sono forniti in **formato JSON**, facilmente integrabile nel backend.

> **Nota:** pur essendo orientata al mondo delle scommesse, l’API offre endpoint utili per scopi informativi e didattici.

---

##  Funzionalità principali dell’applicazione

### 1. Risultati delle partite
- Visualizzazione dei risultati recenti.
- Elenco delle partite in programma.
- Stato dell’evento (in corso, terminato, programmato).

### 2. Eventi giornalieri
- Lista degli eventi sportivi della giornata.
- Informazioni principali:
  - squadre partecipanti;
  - data e ora;
  - sport e campionato.

### 3. Dettaglio evento
- Risultato finale o parziale.
- Stato dell’evento.
- Data e ora di svolgimento.

### 4. Filtri
- Filtro per sport.
- Filtro per campionato (Serie A, NBA, ecc.).
- Filtro temporale (eventi recenti).

---

## ⭐ Feature personalizzata: Statistiche squadra
Cliccando sul nome di una squadra, l’utente accede a una **scheda statistica dedicata**, che mostra:

### Statistiche disponibili
- **Gol fatti totali**
- **Gol subiti totali**
- **Gol fatti in casa**
- **Gol subiti in casa**
- **Gol fatti in trasferta**
- **Gol subiti in trasferta**
- **Partite vinte**
- **Partite pareggiate**
- **Partite perse**

###  Obiettivo della feature
Questa funzionalità permette di:
- analizzare l’andamento stagionale della squadra;
- confrontare le prestazioni tra casa e trasferta;
- arricchire la semplice visualizzazione dei risultati con un contesto statistico reale.

---

## Architettura del sistema

### Backend
Il backend funge da intermediario tra ESPN API e frontend.

Responsabilità:
- gestione sicura della chiave API;
- chiamate agli endpoint ESPN;
- normalizzazione dei dati;
- calcolo delle statistiche di squadra;
- esposizione di endpoint REST.

#### 📌 Esempi di endpoint
