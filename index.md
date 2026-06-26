---
layout: home
title: "Bergadano Didattica — Liceo Vittoria"
---

<header class="hero">
  <p class="hero-eyebrow">Liceo Vittoria · Torino</p>
  <h1 class="hero-title">Matematica e Fisica,<br><em>spiegati insieme</em></h1>
  <p class="hero-subtitle">
    Materiale didattico interattivo per i corsi del Prof. Fulvio Bergadano.
    Scegli la tua classe per accedere agli appunti, simulazioni ed esercizi.
  </p>
  <div class="hero-formula" aria-label="Alcune formule dei corsi">
    \( i\hbar\,\frac{\partial}{\partial t}\Psi = \hat{H}\Psi \)
    &ensp;·&ensp;
    \( \nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0} \)
    &ensp;·&ensp;
    \( \lim_{x\to 0}\frac{\sin x}{x} = 1 \)
  </div>
</header>

<main class="courses-section">
  <div class="courses-group">
    <h2 class="courses-group-title">Scegli la tua classe</h2>
    <div class="classi-grid">
      {% for classe in site.data.classi %}
      <a href="{{ '/classi/' | append: classe.id | append: '/' | relative_url }}" class="classe-card">
        <p class="classe-card-label">Anno {{ classe.anno }}</p>
        <p class="classe-card-nome">{{ classe.nome }}</p>
        <ul class="classe-card-corsi">
          {% for corso in classe.corsi %}
          <li class="materia-{{ corso.materia }}">{{ corso.nome }}</li>
          {% endfor %}
        </ul>
        <span class="card-arrow" aria-hidden="true">→</span>
      </a>
      {% endfor %}
    </div>
  </div>
</main>

<section class="info-strip">
  <div class="info-strip-inner">
    <div class="info-item">
      <p class="info-item-label">Docente</p>
      <p class="info-item-value">Prof. Fulvio Bergadano</p>
    </div>
    <div class="info-item">
      <p class="info-item-label">Istituto</p>
      <p class="info-item-value">Liceo Vittoria · Torino</p>
    </div>
    <div class="info-item">
      <p class="info-item-label">Materie</p>
      <p class="info-item-value">Matematica · Fisica · Cittadinanza</p>
    </div>
    <div class="info-item">
      <p class="info-item-label">Anno scolastico</p>
      <p class="info-item-value">2025–2026</p>
    </div>
  </div>
</section>
