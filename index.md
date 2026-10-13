---
layout: default
title: Главная
permalink: /
---

<section class="hero">
  <h1 class="hero-brand">
    {% include clew-mark.html size="hero" %}
    <span class="hero-brand-text">SciClew</span>
  </h1>
  <p class="lede">Отбираем значимые темы и обсуждаем их вместе — без потока всего подряд.</p>
  <p class="hero-cta">
    <a href="{{ '/meetings/' | relative_url }}">Встречи</a>
    <span class="hero-cta-sep" aria-hidden="true">·</span>
    <a href="{{ '/notes/' | relative_url }}">Заметки</a>
    <span class="hero-cta-sep" aria-hidden="true">·</span>
    <a href="{{ '/books/' | relative_url }}">Книги</a>
  </p>
</section>

<section class="section">
  <h2>О клубе</h2>
  <p>Информационный канал и площадка для спокойных, содержательных разговоров о науке и математике. Мы собираем материалы, которые стоит обсудить, и встречаемся, чтобы разобрать их вместе.</p>
</section>

<section class="section">
  <h2>Темы</h2>
  <ul class="topic-list">
    <li><strong>Jev</strong>, <strong>JEPA</strong>, <strong>RL</strong> (reinforcement learning)</li>
    <li>теория принятия решений</li>
    <li>теория вероятностей и статистика</li>
    <li>математические дискуссии</li>
  </ul>
</section>

<section class="section">
  <h2>Как участвовать</h2>
  <ol class="plain-list">
    <li>Следите за <a href="{{ '/meetings/' | relative_url }}">встречами</a> — даты, темы и повестка.</li>
    <li>Читайте <a href="{{ '/notes/' | relative_url }}">заметки</a> по обсуждениям и материалам.</li>
    <li>Заглядывайте в <a href="{{ '/books/' | relative_url }}">книги</a> — отобранные источники и выдержки.</li>
  </ol>
  <p class="note-aside">Формат камерный и кураторский: лучше одна сильная тема, чем десяток случайных ссылок.</p>
</section>
