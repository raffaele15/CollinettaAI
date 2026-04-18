# CollinettaAI

Manuale di reparto per gli specializzandi in Neurologia della Clinica Neurologica AOPD. App single-page statica che legge e scrive contenuti direttamente su GitHub tramite API, con autenticazione locale cifrata.

## Caratteristiche

- **Single file HTML** — nessun backend, tutto client-side
- **Auth Lettera.AI-style** — GitHub PAT cifrato AES-GCM con passphrase per-utente (decifrato al login, tenuto solo in sessionStorage)
- **Editor WYSIWYG** — Toast UI Editor, esperienza tipo Word/LibreOffice, salva come Markdown
- **Form strutturati** per metadati (titolo, tag, relazioni)
- **Rubrica telefonica** con filtri per guardia/urgenza e tap-to-copy
- **Lock advisory** — previene 95% dei conflitti mostrando "file in modifica da X"
- **Soft delete** — file eliminati finiscono in `/cestino/`, ripristinabili con gestione collisioni
- **Conflict detection** su SHA — se due utenti editano la stessa risorsa, viene offerta Ricarica/Sovrascrivi
- **Search fuzzy globale** (Fuse.js) con shortcut Cmd/Ctrl+K
- **Print-friendly** — ogni pagina è stampabile con CSS media print

## Setup iniziale (una tantum, da admin)

### 1. Fork e configura il repo

1. Fai fork di questo repo sul tuo account GitHub (o crealo da zero con questa struttura)
2. Nel file `index.html` cerca `const CONFIG = {` (riga ~370 circa) e aggiorna:
   ```javascript
   REPO_OWNER: 'tuo-username',
   REPO_NAME: 'CollinettaAI',
   BRANCH: 'main',
   ```
3. Attiva GitHub Pages: Settings → Pages → Source: `main` branch, root
4. Il repo **deve essere pubblico** — i moduli e le procedure sono accessibili via GitHub Pages

### 2. Genera il GitHub PAT

1. Vai su https://github.com/settings/personal-access-tokens/new
2. Token name: `CollinettaAI`
3. Expiration: max 1 anno
4. Repository access: *Only select repositories* → solo `CollinettaAI`
5. Permissions → Repository permissions → **Contents: Read and write** (tutto il resto resta "No access")
6. Genera il token e **copialo subito** (GitHub non lo mostrerà più)

### 3. Cifra il token per ogni utente

1. Apri `setup.html` nel browser (puoi farlo dal disco senza deployare)
2. Per ogni specializzando che deve poter modificare:
   - Inserisci username (es. `dr.rossi`) — solo lettere, cifre, punto, trattino
   - Passphrase (stessa per tutti, da condividere offline)
   - Incolla il PAT
   - Click "Cifra e aggiungi al file"
3. Click "Scarica encrypted-tokens.json"
4. Committa il file in `data/encrypted-tokens.json` nel repo

### 4. Distribuisci l'accesso

- URL app: `https://tuo-username.github.io/CollinettaAI/`
- Username: quelli creati al punto 3
- Passphrase: condivisa via canale sicuro (Signal, di persona, non in chat)

## Struttura del repository

```
CollinettaAI/
├── index.html                       ← app principale
├── setup.html                       ← admin tool (può vivere fuori repo)
├── README.md
├── content/
│   ├── procedure/
│   │   ├── rachicentesi.md
│   │   └── ...
│   ├── moduli/
│   │   ├── consenso-rachicentesi.md
│   │   └── img/
│   │       └── *.webp
│   ├── tabelle/
│   │   └── *.md
│   └── numeri.yml
├── cestino/                         ← soft-deleted files
│   └── procedure/
├── data/
│   └── encrypted-tokens.json        ← blob cifrati per-utente
├── locks.yml                        ← advisory locks, gestito dall'app
└── scripts/
    └── migrate-docx.py              ← migrazione dal manuale Word (TODO)
```

## Schema dati

### Procedura (`content/procedure/*.md`)

Frontmatter YAML + corpo Markdown:

```yaml
---
id: rachicentesi
titolo: Rachicentesi
tag: [procedura, liquor, diagnostica]
categoria: procedure-reparto
tempo_esecuzione_min: 30
moduli_correlati: [consenso-rachicentesi]
tabelle_correlate: [anticoagulanti-rachicentesi]
procedure_correlate: []
numeri_correlati: [lab-neurologia]
termini_equivalenti: [puntura lombare, LP, LCR]
ultima_modifica: 2026-04-18T14:00:00Z
modificato_da: raffaele.z
cronologia_recente:
  - {data: 2026-04-18T14:00:00Z, utente: raffaele.z, nota: "nota breve"}
---

## Sezione 1
Testo Markdown libero con heading, liste, tabelle, blockquote...
```

### Numeri (`content/numeri.yml`)

File unico YAML con gruppi e contatti. Tag supportati: `guardia`, `urgenza`, `laboratorio`, etc. Campo `procedure_correlate` per bidirezionalità.

### Tabelle (`content/tabelle/*.md`)

Stesso formato procedure, più il campo `tabella_strutturata` opzionale nel frontmatter che duplica i dati in forma leggibile da LLM:

```yaml
tabella_strutturata:
  - farmaco: Warfarin
    tempistica_sospensione: "INR < 1.4-1.5"
```

## Scope v1 — implementato

- Login con decifratura
- Home con procedure, modifiche recenti, accesso rapido
- Vista procedura renderizzata con metadati, tag, relazioni
- Editor procedure con Toast UI WYSIWYG + form metadati
- Save con lock + conflict detection + override
- Vista numeri con filtri guardia/urgenza, tap-to-copy
- Vista moduli (senza upload immagini ancora)
- Vista tabelle renderizzate
- Cestino con soft delete, ripristino, gestione collisioni di nome
- Search fuzzy globale (Cmd/Ctrl+K)
- Refresh manuale

## Scope v1.1 — pianificato

- Upload immagini moduli con compressione WebP client-side
- Editor form dedicato per rubrica numeri
- Conflict resolution a livello di sezione (split per `##` heading)
- Creazione nuove procedure direttamente dall'app
- GitHub Actions per build automatico di `knowledge-base.json` (AI-ready)
- Script Python per migrazione automatica dal `.docx` originale
- Delta refresh (poll differenziale dei commit recenti)
- Glossario sinonimi clinici (`data/glossario.yml`)

## Rotazione passphrase (admin)

Se un utente dimentica la passphrase o va ruotata:

1. Apri `setup.html`, carica `encrypted-tokens.json` attuale
2. Inserisci lo username, nuova passphrase, stesso PAT
3. Click "Cifra e aggiungi" → il blob dell'utente viene sostituito, gli altri invariati
4. Scarica e ricommitta

Per ruotare il PAT (compromissione sospetta): revoca il vecchio PAT su GitHub, genera nuovo PAT, rigenera i blob di tutti gli utenti con il nuovo PAT mantenendo le loro passphrase.

## Note di sicurezza

- Il blob cifrato vive nel repo pubblico ma è inutilizzabile senza passphrase
- PBKDF2-SHA256 con 250000 iterazioni rende infattibile un brute-force della passphrase da parte di un attaccante
- Il token in chiaro vive SOLO in `sessionStorage` (RAM del tab), mai su disco
- Chiusura del tab = logout automatico
- Nessun dato paziente deve MAI essere committato nel repo. I moduli contengono solo template vuoti. La fase 2 (form filling offline con dati paziente) tiene i dati esclusivamente in browser.

## AI-friendliness

Lo schema è progettato per supportare in futuro Q&A/RAG senza rifattorizzazioni:

- ID stabili e URL-safe per ogni entità
- Breadcrumb impliciti nei heading `##`
- Relazioni bidirezionali (`moduli_correlati`, `numeri_correlati`, etc.)
- Termini equivalenti / sinonimi clinici
- Tabelle disponibili in forma strutturata oltre che Markdown
- Provenienza e cronologia per ogni modifica

Un futuro script di build produrrà `data/knowledge-base.json` con chunking semantico pronto per essere indicizzato da un retriever.

## Troubleshooting

**"Impossibile caricare encrypted-tokens.json"** → il repo non è pubblico, oppure il file non esiste ancora. Verifica entrambi.

**"Token non valido (HTTP 401/403)"** → il PAT è scaduto o revocato. Rigenera tramite `setup.html`.

**"Conflict" al salvataggio** → un altro utente ha salvato mentre editavi. Usa "Ricarica e riapplica" o "Sovrascrivi".

**L'editor non apre** → Toast UI Editor è caricato da CDN. Controlla la console per errori di rete.

**Le modifiche non appaiono per altri utenti** → GitHub Pages impiega 60-90s per ricompilare. L'app legge direttamente dall'API GitHub (non da Pages), quindi la Refresh nel topbar forza un reload immediato senza aspettare Pages.
