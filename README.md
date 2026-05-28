# Starcks × DomusBet — Proposta commerciale 2026

Deck statico a pagina singola ("Le tre strade") per la proposta Starcks Betting 2026 a
DomusBet. Nessun build step: HTML autonomo, immagini in base64 inline, CSS e JS tutto nel
file. Si pubblica così com'è.

---

## Pubblicazione (GitHub → Netlify) https://app.netlify.com/projects/domusbet2026/overview

Il repo è collegato a Netlify: ogni push/upload sul branch principale fa partire il deploy
automatico.

- **`index.html`** è la homepage servita da Netlify in root. È la copia da pubblicare.
- **`offerta-domusbet.html`** è la stessa identica pagina col nome esplicito (backup /
  riferimento). Non serve a Netlify, è solo comodità.

Per aggiornare il deck: rigenera l'HTML, sostituisci sia `index.html` sia
`offerta-domusbet.html`, fai push. Fine.

Peso `index.html`: ~5,1 MB (9 immagini uniche in base64 inline — 6 screenshot app + 3 della
piattaforma Starcks — ripetute nei caroselli). Normale per questo tipo di deck: è il prezzo
di avere tutto inline e zero dipendenze esterne.

---

## Cosa contiene il deck — Le tre strade

Tre offerte affiancate, ognuna con card espandibile (clic sulle voci per il dettaglio):

### Offerta 01 — Starcks 360 (esclusiva)
Sponsorship esclusiva sull'ecosistema proprietario Starcks: community ZonaFanta + community
tipster Zona1x2 + piattaforma di gamification + app white-label. Non si costruisce nulla di
nuovo: si vende accesso esclusivo ad asset già attivi. **180.000€ + IVA a stagione.**

### Offerta 02 — Social di DomusBet
Si costruisce da zero l'ecosistema social del brand: lancio profilo istituzionale,
rebranding di una community fanta acquisita, motore organico di video su 120 profili, app
inclusa. Pricebox **interattivo**: i toggle attivano/disattivano le voci opzionali (motore
video, server app, boost community) e ricalcolano il totale. **9.500€/mese + IVA + 11.000€
una tantum** (configurazione piena).

### Offerta 03 — Boost Affiliazioni (solo DomusBet)
Affiliazione pura, esclusiva di questo brand. FantaDomusBet dato gratis e agganciato **dentro
DomusBet**: le giocate nel fanta sganciano free spin, free bonus e real bonus sul conto.
Modello economico in **revenue share su NGR** sui player portati; setup 2.000€ una tantum;
fee server ~1.500€/mese **che scende fino a zero** in base alla % di rev share. Toggle sul
boost community opzionale (+9.000€ una tantum).

Compliance di questa offerta = **modello Sisal Tipster**: landing pubblica
`fantadomusbet.it` come vetrina, ma il game gira dentro DomusBet ed è accessibile **solo a
utente loggato**, nell'ambiente ADM già autorizzato. Niente cuscinetto for-fun — qui non
serve.

In fondo, la sezione **"La differenza, in chiaro"** mette le tre strade a confronto e spiega
che possono convivere.

---

## ⚠️ Cosa NON modificare (asset proprietari Starcks)

Questi elementi sono di Starcks, **non** del cliente. Restano sempre col loro nome e aspetto,
per qualsiasi brand:

- **Verde acqua `#2bc5ad`** — è il colore di Starcks. Non si tocca mai.
- **Logo Starcks** e i nomi "Starcks", "Starcks 360", "Starcks Store", "Starcks Game/League".
- **Community ZonaFanta**, community tipster **Zona1x2**, community Starcks e tutti i loro
  link social.
- **Le 3 immagini della piattaforma** (Starcks The Game / formazione / League): sono uno
  screenshot reale della stagione passata brandizzato **NetBet.sport**, usato come case study
  ("ecco la piattaforma già brandizzata con uno sponsor betting"). Il brand NetBet visibile è
  voluto: è la prova di un lavoro reale già fatto. Valgono per ogni cliente.
- **Tutti i numeri** (prezzi, totali, reach, CPM, video, view): sono fissi e identici per
  ogni brand, già allineati ai valori safe (+5M view/mese, +7.000 video/mese). Non si
  modificano.

Si ribrandizza **solo** ciò che è del cliente: nome brand, app, dominio, handle social,
colore accent, screenshot dell'app del brand.

---

## Note tecniche

- **Generazione:** il deck base (Offerta 01 + 02) esce dalla skill
  `offerta-2026-starcks-betting`. La **Offerta 03 — Boost Affiliazioni** è specifica di
  DomusBet ed è stata aggiunta in post-produzione sull'HTML generato (la skill produce solo
  360 + Social). Se diventa ricorrente per altri brand, va valutata come estensione skill.
- **Fondo pagina:** nero (palette override), coerente con l'app DomusBet (nero + rosso +
  bianco). Accent brand: rosso `#C61C36` (hover `#a8152c`).
- **Griglia:** 3 colonne sopra 1080px → 2 colonne tra 820 e 1080px → 1 colonna sotto 820px.
- **Interattività:** i pricebox di Social e Affiliazioni hanno toggle indipendenti. Tutto in
  vanilla JS inline, nessuna libreria.
- I link "Deep dive dei contenuti" puntano al Google Sheet DomusBet; il bottone "Prova la
  demo" al prototipo Figma DomusBet.

---

## Da confermare / aperto

- **Handle istituzionale `@domusbet.tv`** — di default = dominio cuscinetto, da confermare col
  brand (potrebbe essere `@domusbet` secco). Se cambia, rigenerare.
- **% di revenue share** dell'Offerta 03 — nel deck è scritta come "% sui player portati",
  senza numero. Quando concordata, si può inserire la cifra.
- **Screenshot Offerta 03** — il carosello della terza card usa i primi 4 dei 6 screenshot
  app. Modificabile su richiesta (ordine diverso o tutti e 6).
