---
layout: default
title: Главная
permalink: /
---

{% assign meetings = site.meetings | sort: 'date' | reverse %}
{% assign latest = meetings | first %}
{% assign shelf = site.books | where_exp: 'book', 'book.placeholder != true' | sort: 'title' %}

<section class="hero-grid">
  <div class="hero-copy">
    <h1>Научный дискуссионный клуб</h1>
    <p class="kicker">sandbox · тбилиси</p>
    <p class="lede">Отбираем значимые темы и обсуждаем их вместе — без потока всего подряд.</p>
    <p class="hero-actions">
      {% if latest %}
      <a class="button" href="{{ latest.url | relative_url }}">К встрече</a>
      {% else %}
      <a class="button" href="{{ '/meetings/' | relative_url }}">Встречи</a>
      {% endif %}
      <a class="text-link" href="{{ '/books/' | relative_url }}">Книги</a>
    </p>
  </div>

  {% if latest %}
  {% assign meeting_day = latest.date | date: '%Y%m%d' | plus: 0 %}
  {% assign today = site.time | date: '%Y%m%d' | plus: 0 %}
  <aside class="panel">
    <p class="panel-label">
      {% if meeting_day > today %}ближайшая встреча
      {% elsif meeting_day == today %}встреча сегодня
      {% else %}последняя встреча{% endif %}
    </p>
    <h2 class="panel-title"><a href="{{ latest.url | relative_url }}">{{ latest.title }}</a></h2>
    {% if latest.date %}
    <p class="panel-meta"><time datetime="{{ latest.date | date: '%Y-%m-%d' }}">{{ latest.date | date: '%d.%m.%Y' }}</time></p>
    {% endif %}
    {% if latest.excerpt %}
    <p class="panel-text">{{ latest.excerpt }}</p>
    {% endif %}
    <p class="panel-more"><a class="text-link" href="{{ latest.url | relative_url }}">Читать разбор</a></p>
  </aside>
  {% endif %}
</section>

<section class="split">
  <div>
    <h2>О клубе</h2>
    <p>Площадка для спокойных разговоров о науке и математике. Одна сильная тема за встречу, со ссылками на источники.</p>
  </div>
  {% if shelf.size > 0 %}
  <div>
    <h2>К чтению</h2>
    <ul class="item-list">
      {% for book in shelf limit: 3 %}
      <li>
        <span class="item-meta">
          {% if book.author %}{{ book.author }}{% endif %}
          {% if book.kind == 'link' %} · внешняя ссылка{% elsif book.kind == 'onsite' %} · на сайте{% endif %}
        </span>
        <a class="item-title" href="{{ book.url | relative_url }}">{{ book.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>
  {% endif %}
</section>

<div class="bands">
  <section class="band">
    <h2>Где</h2>
    <div>
      <p>Клуб собирается в <a href="https://sandb0x.space/">sandbox</a>.</p>
      <p><a href="https://sandb0x.space/#visit">Как прийти</a></p>
    </div>
  </section>
</div>
