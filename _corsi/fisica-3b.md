---
layout: corso
title: "Fisica 3ª B"
classe: "3B"
materia: fisica
capitoli_lista:
  - numero: 1
    titolo: "Grandezze fisiche e misure"
  - numero: 2
    titolo: "La cinematica"
  - numero: 3
    titolo: "Le forze e la dinamica"
  - numero: 4
    titolo: "Lavoro ed energia"
  - numero: 5
    titolo: "Quantità di moto"
  - numero: 6
    titolo: "Moto circolare e gravitazione"
---

<header class="course-hero">
  <span class="course-tag">Fisica · 3° anno · Classe 3B</span>
  <h1 class="course-title">Fisica 3ª B</h1>
  <p class="course-desc">
    Introduzione alla fisica classica: dalla misura delle grandezze fisiche
    alla meccanica newtoniana, passando per cinematica, dinamica ed energia.
  </p>
</header>

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- CAPITOLO 1                                                      -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<section id="cap1" class="chapter-section">
<header class="chapter-header">
  <span class="chapter-number">Capitolo 1</span>
  <h2 class="chapter-title">Grandezze fisiche e misure</h2>
</header>
<div class="prose">

La fisica è una scienza sperimentale: ogni affermazione deve essere verificata
attraverso misure. In questo capitolo introduciamo il concetto di grandezza fisica,
le unità di misura del Sistema Internazionale e le nozioni di errore e cifre significative.

{% include box-def.html titolo="Grandezza fisica" %}
Una **grandezza fisica** è una proprietà di un corpo o di un fenomeno
che può essere misurata, ovvero confrontata con un campione della stessa natura
(unità di misura). Formalmente, una misura è una coppia (valore numerico, unità):
$$L = 3{,}2\,\text{m}$$
{% include box-end.html %}

### Il Sistema Internazionale di Unità (SI)

Il SI definisce sette grandezze fondamentali, da cui si derivano tutte le altre.

{% include box-thm.html titolo="Grandezze fondamentali del SI" %}
Lunghezza: metro (m) &emsp;·&emsp;
Massa: chilogrammo (kg) &emsp;·&emsp;
Tempo: secondo (s) &emsp;·&emsp;
Corrente elettrica: ampere (A) &emsp;·&emsp;
Temperatura: kelvin (K)
{% include box-end.html %}

{% include box-warn.html titolo="Massa ≠ Peso" %}
Non confondere *massa* e *peso*: la massa è una proprietà intrinseca
del corpo (kg), il peso è una forza ($\vec{P} = m\vec{g}$, misurata in Newton).
{% include box-end.html %}

### Errori di misura

Ogni misura è affetta da incertezza. Il risultato si esprime come:

$$x = x_0 \pm \Delta x$$

dove $x_0$ è il valore misurato e $\Delta x$ è l'**incertezza assoluta**.
L'**errore relativo** è invece il rapporto adimensionale $\Delta x / x_0$.

{% include fill-def.html id="def-errore-relativo"
   prompt="Scrivi con parole tue la differenza tra errore assoluto ed errore relativo, e spiega quando uno è più utile dell'altro." %}

{% include box-ex.html titolo="Esempio 1.1 — Errore relativo" %}
Ho misurato la lunghezza di un tavolo: $L = (1{,}254 \pm 0{,}001)\,\text{m}$.
L'errore relativo è:
$$\frac{\Delta L}{L} = \frac{0{,}001}{1{,}254} \approx 0{,}08\%$$
{% include box-end.html %}

### Esercizi

**Esercizio 1.1.** Un corpo viene pesato tre volte:
$m_1 = 2{,}43\,\text{kg}$, $m_2 = 2{,}46\,\text{kg}$, $m_3 = 2{,}44\,\text{kg}$.
Calcola la media e l'errore assoluto (semidispersione massima).

{% include spoiler.html testo="Mostra la soluzione dell'esercizio 1.1" %}
**Media:**
$$\bar{m} = \frac{2{,}43 + 2{,}46 + 2{,}44}{3} = 2{,}443\,\text{kg}$$

**Semidispersione massima:**
$$\Delta m = \frac{m_{\max} - m_{\min}}{2} = \frac{2{,}46 - 2{,}43}{2} = 0{,}015\,\text{kg}$$

**Risultato:** $m = (2{,}44 \pm 0{,}02)\,\text{kg}$
{% include spoiler-end.html %}

{% include video.html id="ZM8ECpBuQYE" didascalia="Introduzione alle grandezze fisiche e al SI (fonte esterna)" %}

{% include homework.html
   titolo="Compito — Capitolo 1"
   descrizione="Risolvi gli esercizi sulle misure e gli errori. Consegna entro venerdì."
   link="https://forms.google.com/INSERISCI-LINK" %}

</div>
</section>

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- CAPITOLO 2                                                      -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<section id="cap2" class="chapter-section">
<header class="chapter-header">
  <span class="chapter-number">Capitolo 2</span>
  <h2 class="chapter-title">La cinematica</h2>
</header>
<div class="prose">

La cinematica descrive il *come* si muovono i corpi, senza occuparsi delle cause del moto.

{% include box-def.html titolo="Velocità media" %}
La **velocità media** nell'intervallo $[t_1, t_2]$ è:
$$\bar{v} = \frac{\Delta x}{\Delta t} = \frac{x(t_2) - x(t_1)}{t_2 - t_1}$$
La velocità *istantanea* è il limite per $\Delta t \to 0$:
$$v(t) = \frac{dx}{dt} = \dot{x}$$
{% include box-end.html %}

<!-- SIMULAZIONE INTERATTIVA — generata da Claude su richiesta -->
<!-- Per aggiungere una simulazione, scrivi a Claude:            -->
<!-- "Aggiungi una simulazione del moto rettilineo uniforme      -->
<!--  al capitolo 2 di Fisica 3B"                               -->

{% include box-thm.html titolo="Moto uniformemente accelerato (MUA)" %}
Con accelerazione costante $a$, posizione iniziale $x_0$, velocità iniziale $v_0$:
$$x(t) = x_0 + v_0\,t + \frac{1}{2}a\,t^2$$
$$v(t) = v_0 + a\,t$$
$$v^2 = v_0^2 + 2a\,(x - x_0)$$
{% include box-end.html %}

{% include box-note.html titolo="Caduta libera" %}
La caduta libera è un MUA con $a = g \approx 9{,}81\,\text{m/s}^2$
(verso il basso) e $v_0 = 0$ (se il corpo parte da fermo).
{% include box-end.html %}

</div>
</section>

<!-- Capitoli 3-6: aggiungi il contenuto via via -->

<section id="cap3" class="chapter-section">
<header class="chapter-header">
  <span class="chapter-number">Capitolo 3</span>
  <h2 class="chapter-title">Le forze e la dinamica</h2>
</header>
<p style="color:#718096;font-style:italic;">Contenuto in preparazione.</p>
</section>

<section id="cap4" class="chapter-section">
<header class="chapter-header">
  <span class="chapter-number">Capitolo 4</span>
  <h2 class="chapter-title">Lavoro ed energia</h2>
</header>
<p style="color:#718096;font-style:italic;">Contenuto in preparazione.</p>
</section>

<section id="cap5" class="chapter-section">
<header class="chapter-header">
  <span class="chapter-number">Capitolo 5</span>
  <h2 class="chapter-title">Quantità di moto</h2>
</header>
<p style="color:#718096;font-style:italic;">Contenuto in preparazione.</p>
</section>

<section id="cap6" class="chapter-section">
<header class="chapter-header">
  <span class="chapter-number">Capitolo 6</span>
  <h2 class="chapter-title">Moto circolare e gravitazione</h2>
</header>
<p style="color:#718096;font-style:italic;">Contenuto in preparazione.</p>
</section>
