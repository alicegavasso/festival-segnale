# Resoconto del lavoro con l’AI

## Sessione 1

### 1.1
- Ho chiesto di creare `dati/SCHEMA.md` per le entità Evento e Sede.
- Ho usato i due JSON iniziali per ricavare campi, tipi, esempi, chiavi primarie e relazione.
- Ho verificato che fossero presenti quantità, aggiornamento dati, descrizione della pagina e schema Mermaid.
- Non ho scartato contenuti importanti, solo reso il testo più ordinato.

### 1.2
- Ho chiesto di far caricare `programma.html` con `fetch` dai file JSON.
- Ho usato i dati per creare le schede in modo dinamico e mostrare il nome della sede.
- Ho verificato i messaggi per caricamento, errore e assenza di eventi.
- Ho avuto il problema della scritta “Caricamento in corso” che restava visibile.
- L’ho risolto correggendo la parte che nasconde il messaggio dopo il caricamento.

### 1.3
- Ho chiesto di sistemare `programma.html` con il foglio di stile già presente.
- Ho controllato la struttura delle cartelle e i percorsi dei file JSON.
- Ho chiarito dove inserire `fetch('dati/eventi.json')` e `fetch('dati/sedi.json')`.
- Ho verificato che il problema non dipendesse dai file, ma dal codice.

### 1.4
- Ho chiesto di aggiungere in `info.html` una sezione meteo con dati da Open-Meteo.
- Ho usato l’API per mostrare temperatura, vento, ora del dato e fonte.
- Ho aggiunto anche lo stile del riquadro meteo in `style.css`.
- Ho verificato che un errore dell’API non bloccasse il resto della pagina.

### 1.5
- Ho chiesto perché su GitHub Pages la sezione meteo non si vedeva correttamente.
- Ho controllato file aggiornati, script, CSS e cache del browser.
- Ho concluso che il problema era nel deploy o nell’aggiornamento della pagina.
- Ho suggerito di rifare la pubblicazione e forzare il refresh.