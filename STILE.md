# STILE.md — Guida ai colori e al font del sito
## Documento di contesto per Claude (Project knowledge)
*Carica questo file nel Project knowledge insieme a PROGETTO.md.*
*Quando cambi i colori, aggiorna questo file e ricaricalo.*

---

## Stato attuale dei colori

Tutti i valori sono in `_sass/STILE.scss`. Questa è la versione corrente:

### Colori principali

| Variabile SCSS | Valore hex | Ruolo |
|---|---|---|
| `$cyan` | `#0891b2` | Accento principale, Matematica, link hover |
| `$teal` | `#0f766e` | Accento secondario, Fisica, sidebar |
| `$magenta` | `#c026d3` | Link, pulsanti di consegna |
| `$citt-accent` | `#7c3aed` | Cittadinanza e Prospettive Globali |

### Colori per materia (card e accenti)

| Materia | Accento | Sfondo card | Bordo card |
|---|---|---|---|
| Matematica | `#0891b2` (cyan) | `#e0f2fe` | `#7dd3fc` |
| Fisica | `#0f766e` (teal) | `#f0fdf4` | `#86efac` |
| Cittadinanza | `#7c3aed` (viola) | `#faf5ff` | `#d8b4fe` |

### Colori dei box di contenuto

| Box | Sfondo | Bordo sinistro |
|---|---|---|
| Definizione | `#e0f7fa` (cyan pastello) | `#0891b2` |
| Teorema | `#f0fdf4` (teal pastello) | `#0f766e` |
| Attenzione | `#fefce8` (giallo pastello) | `#ca8a04` |
| Esempio | `#faf5ff` (viola pastello) | `#7c3aed` |
| Dimostrazione | `#f8fafc` (grigio chiarissimo) | `#718096` |
| Nota | `#fff7ed` (arancio pastello) | `#ea580c` |

### Font

| Ruolo | Font | Note |
|---|---|---|
| Corpo del testo | Source Serif 4 | Font principale, stile Mathpazo-like |
| Titoli e intestazioni | IM Fell English | Font display, carattere classico |
| Accessibilità | Atkinson Hyperlegible | Attivato dal pulsante "Aa leggibilità" |
| Monospace (codice) | JetBrains Mono | Per eventuali blocchi di codice |

---

## Come cambiare un colore

Apri `_sass/STILE.scss` e modifica il valore hex della variabile che vuoi cambiare.
Poi esegui `git add . && git commit -m "nuovo colore" && git push`.

Oppure di' a Claude: *"Cambia il colore della Matematica dal cyan al blu #1d4ed8"*
e Claude ti darà le righe precise da modificare in `STILE.scss`.

---

## Preferenze estetiche del docente

- Palette pastello: sfondi chiari, bordi colorati ma non invadenti
- Tinte principali: cyan/teal come base, con accenti magenta per i link
- Niente colori saturi o sgargianti come sfondo principale
- Il sito deve sembrare un documento tipografico curato, non un'app moderna
- Font corpo simile a Mathpazo (serif, elegante, leggibile per testi lunghi)
- Titoli con personalità tipografica (IM Fell English ha un carattere storico/accademico)

---

## Cronologia delle modifiche di stile

*(aggiorna questa sezione ogni volta che cambi qualcosa)*

| Data | Modifica |
|---|---|
| 2025-06 | Prima versione — palette cyan/teal/magenta su sfondo #fafaf8 |
