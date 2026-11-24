# NicolausFlat: sito statico che porta all'annuncio Airbnb

## Cosa c'è nello zip
- 7 pagine in italiano: `index.html`, `appartamento.html`, `come-arrivare.html`, `guida-bari.html`, `gite-da-bari.html`, `faq.html`, `prenota.html`
- 4 pagine in inglese in `en/`: `index.html`, `apartment.html`, `faq.html`, `book.html`
- `style.css` (stile condiviso), `robots.txt`, `sitemap.xml`, `llms.txt`
- Dati strutturati JSON-LD (schema.org) nelle pagine: struttura, appartamento (con collegamento `sameAs` all'annuncio Airbnb), FAQ, articoli

Tutti i pulsanti "Prenota su Airbnb" puntano a `https://www.airbnb.it/rooms/43951851`. Non ci sono moduli, pagamenti né raccolta dati.

## 1. Da sostituire prima di pubblicare
| Cosa | Dove | Note |
|---|---|---|
| `www.nicolausflat.it` | tutti i file, `sitemap.xml`, `robots.txt`, `llms.txt` | Sostituisci con il dominio che registri davvero (trova e sostituisci su tutto) |

## 2. Da verificare (commenti `VERIFICA` / `VERIFY` nel codice)
- Capienza massima (nell'annuncio Airbnb: 2 ospiti, ma il testo cita il divano letto per più persone)
- Tariffe e orari della sosta nella Zona sosta regolamentata A e dei parcheggi
- Trasporto aeroporto-stazione: aggiungi il servizio che consigli e i tempi aggiornati
- Regole su animali, fumo, feste e check-out nelle FAQ, se vuoi indicarle
- Nome del vicolo o di un locale che consigli per le orecchiette, in `guida-bari.html`
- Dati delle recensioni (4,99 su 5 in 268 recensioni, novembre 2026): aggiornali ogni tanto

## 3. Foto
Crea la cartella `img/` e aggiungi le tue foto, poi inserisci i tag `<img>` nei punti indicati dai commenti. Usa nomi file descrittivi (es. `soggiorno-bari-divano-letto.jpg`), testo `alt` descrittivo e comprimi le immagini (meglio sotto i 300 KB ciascuna). Non copiare le foto dalla pagina Airbnb se non sono tue.

## 4. Pubblicare gratis
1. Registra il dominio presso un registrar (circa 10-15 € l'anno, verifica il prezzo).
2. Crea un account su **Cloudflare Pages**, **Netlify** o **GitHub Pages**.
3. Carica la cartella (su Netlify basta trascinarla nella pagina "Deploys").
4. Collega il dominio seguendo le istruzioni del servizio. HTTPS è incluso.

## 5. Dopo la pubblicazione
- Inserisci il sito nel tuo **Google Business Profile** (campo sito web).
- Iscrivi il sito a **Google Search Console**, invia `sitemap.xml` e richiedi l'indicizzazione delle pagine principali. Search Console è anche il modo per misurare le visite, perché Airbnb non ti dirà da dove arrivano gli ospiti.
- Controlla i dati strutturati con il Rich Results Test e con validator.schema.org.
- Aggiungi il sito alle directory turistiche di Bari e della Puglia e, se possibile, a blog e pagine locali che parlano della zona.
- Verifica nei termini per host di Airbnb che un link al tuo annuncio dal tuo sito sia consentito nella forma che usi.

## 6. Note
- Il sito non usa cookie né analytics: non serve il banner cookie. Se aggiungi Google Analytics o simili, ti serve un banner di consenso e una privacy policy.
- Le recensioni sono citate solo in testo, con la fonte. Nel JSON-LD non c'è `aggregateRating` basato su recensioni di terze parti: Google non ne premia l'uso per recensioni prese da altre piattaforme.
- Se in futuro vorrai prenotazioni dirette, servirà aggiungere un modulo o un booking engine, la sincronizzazione dei calendari e una privacy policy.
