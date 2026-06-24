# HOWTO — Guida rapida al sito
*Tutto quello che serve per lavorare ogni giorno. Tienilo aperto.*

---

## Setup iniziale (una volta sola)

```bash
# 1. Clona il repository
git clone https://github.com/[tuousername]/bergadano-didattica.git
cd bergadano-didattica

# 2. Installa le dipendenze Jekyll
bundle install

# 3. Avvia il server locale — il sito si aggiorna automaticamente ad ogni salvataggio
bundle exec jekyll serve
# Poi apri nel browser: http://localhost:4000
```

---

## I 5 comandi di tutti i giorni

```bash
# Avviare l'anteprima locale
bundle exec jekyll serve

# Pubblicare le modifiche su GitHub Pages (il sito si aggiorna in ~60 secondi)
git add .
git commit -m "descrizione breve di cosa hai modificato"
git push

# Vedere cosa hai modificato prima di pubblicare
git status
git diff
```

---

## Come aggiungere contenuto a un capitolo

1. Apri il file del corso in `_corsi/[nome-corso].md`
2. Trova la sezione `<section id="capN" ...>`
3. Scrivi dentro `<div class="prose">` usando Markdown e i tag include

**Formule** — come in LaTeX, solo con `$$` invece di `\[...\]`:
```
Testo con formula inline $\vec{F} = m\vec{a}$ nel paragrafo.

Formula su riga separata:
$$E = mc^2$$
```

**Box colorati:**
```
{% include box-def.html titolo="Nome della definizione" %}
Testo con $formule$.
{% include box-end.html %}
```
I tipi disponibili sono: `box-def` `box-thm` `box-warn` `box-ex` `box-proof` `box-note`

**Esercizio con soluzione nascosta:**
```
Testo dell'esercizio.

{% include spoiler.html testo="Mostra la soluzione" %}
Soluzione qui.
{% include spoiler-end.html %}
```

**Video YouTube:**
```
{% include video.html id="CODICE_VIDEO" didascalia="Descrizione" %}
```
(Il codice video è la parte finale dell'URL: youtube.com/watch?v=**CODICE_VIDEO**)

**Completamento per lo studente:**
```
{% include fill-def.html id="id-univoco" prompt="Scrivi qui la tua domanda" %}
```

**Sezione compiti:**
```
{% include homework.html titolo="Compito N" descrizione="..." link="https://..." %}
```

---

## Come cambiare i capitoli di un corso

Nel front matter YAML in cima al file `.md` del corso:

```yaml
capitoli_lista:
  - numero: 1
    titolo: "Titolo del capitolo 1"
  - numero: 2
    titolo: "Titolo del capitolo 2"
```

La sidebar si aggiorna automaticamente.

---

## Come chiedere una simulazione a Claude

Nel Project "Bergadano Didattica", scrivi:
> "Aggiungi una simulazione di [fenomeno] al capitolo [N] di [corso]"

Specifica:
- Cosa deve mostrare visivamente (un corpo che si muove? un grafico? entrambi?)
- Quali parametri lo studente può controllare con i cursori
- Se vuoi un grafico affiancato (es. posizione vs tempo)

Claude ti darà un blocco di codice da incollare nel punto giusto del file `.md`.

---

## Come convertire i tuoi appunti LaTeX

Nel Project, scrivi:
> "Converti questo LaTeX nel formato del sito per il capitolo [N] di [corso]:"
> [incolla il tuo LaTeX]

Claude tradurrà:
- `\begin{definition}` → `{% include box-def.html ... %}`
- `\begin{theorem}` → `{% include box-thm.html ... %}`
- `\[...\]` → `$$...$$`
- `itemize/enumerate` → elenchi Markdown
- ecc.

---

## Come cambiare i colori

Apri `_sass/STILE.scss` con un editor di testo e modifica i valori hex.
Oppure chiedi a Claude: *"Cambia il colore della Matematica in blu scuro"*.

---

## Struttura dei file (riferimento rapido)

```
_corsi/             ← QUI scrivi il contenuto (un file per corso)
_sass/STILE.scss    ← QUI cambi i colori e i font
_config.yml         ← configurazione generale (raramente)
PROGETTO.md         ← documento per Claude (non serve aprirlo)
STILE.md            ← documento per Claude (aggiornalo quando cambi colori)
```

Tutto il resto **non va toccato** — è gestito da Claude quando necessario.
