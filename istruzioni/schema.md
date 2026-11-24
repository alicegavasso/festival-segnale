# Scheda dati

## Entità

### Evento
Campi:
- `id` — numero intero, esempio: `1`
- `titolo` — stringa, esempio: `"Lettere in movimento"`
- `data` — stringa nel formato `YYYY-MM-DD`, esempio: `"2026-06-12"`
- `orario` — stringa nel formato `HH:MM`, esempio: `"10:00"`
- `categoria` — stringa, esempio: `"Incontro"`
- `descrizione` — stringa, esempio: `"Come cambia un messaggio quando cambiano le lettere? Un incontro su tipografia, ritmo e comunicazione visiva."`
- `immagine` — stringa, esempio: `"assets/lettere-in-movimento.svg"`
- `immagine_alt` — stringa, esempio: `"Lettere geometriche disposte su una griglia"`
- `sede_id` — numero intero, esempio: `1`

Chiave primaria:
- `id` numerico, univoco nell’entità e stabile

### Sede
Campi:
- `id` — numero intero, esempio: `1`
- `nome` — stringa, esempio: `"Sede Centrale"`
- `indirizzo` — stringa, esempio: `"Corso Duca degli Abruzzi 24, Torino"`
- `nome_festival` — stringa, esempio: `"Officina Nord"`
- `immagine` — stringa, esempio: `"assets/luoghi/sede-centrale.jpg"`

Chiave primaria:
- `id` numerico, univoco nell’entità e stabile

## Relazione

Una sede può ospitare più eventi; ogni evento si svolge in una sede.  
`Evento.sede_id` fa riferimento a `Sede.id`.

## Quantità

- Eventi: 6
- Sedi: 3

## Aggiornamento dati

I dati si aggiornano modificando i file JSON nella repository e pubblicando le modifiche.

## Pagina

La pagina mostra gli eventi e le sedi del festival, con i relativi dati descrittivi e il collegamento tra evento e sede.

## Schema Evento–Sede

```mermaid
erDiagram
    SEDE ||--o{ EVENTO : ospita

    SEDE {
        int id PK
        string nome
        string indirizzo
        string nome\_festival
        string immagine
    }

    EVENTO {
        int id PK
        string titolo
        string data
        string orario
        string categoria
        string descrizione
        string immagine
        string immagine\_alt
        int sede\_id FK
    }
