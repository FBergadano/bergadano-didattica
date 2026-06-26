---
layout: capitolo
title: "La cinematica"
corso: fisica-3b
corso_titolo: "Fisica 3ª B"
materia: fisica
classe: "3B"
numero: 2
---

La cinematica descrive il *come* si muovono i corpi, senza occuparsi delle cause del moto.

{% include box-def.html titolo="Velocità media" %}
La **velocità media** nell'intervallo $[t_1, t_2]$ è:
$$\bar{v} = \frac{\Delta x}{\Delta t} = \frac{x(t_2) - x(t_1)}{t_2 - t_1}$$
La velocità *istantanea* è il limite per $\Delta t \to 0$:
$$v(t) = \frac{dx}{dt} = \dot{x}$$
{% include box-end.html %}

### Moto rettilineo uniforme

Nel moto rettilineo uniforme (MRU) la velocità è costante e la posizione varia linearmente nel tempo.

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

### Moto in due dimensioni

Il moto può essere scomposto lungo due assi ortogonali. Ogni componente si studia
indipendentemente.

{% include box-def.html titolo="Moto del proiettile" %}
Un proiettile lanciato con velocità iniziale $v_0$ a angolo $\theta$:

- componente orizzontale: $x(t) = v_0 \cos\theta \cdot t$ (MRU)
- componente verticale: $y(t) = v_0 \sin\theta \cdot t - \frac{1}{2}g\,t^2$ (MUA)
{% include box-end.html %}
