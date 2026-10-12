---
layout: default
title: Заметки
permalink: /notes/
---

# Заметки

<p class="page-lede">Материалы и конспекты обсуждений клуба.</p>

<ul class="item-list">
{% assign notes = site.notes | sort: 'date' | reverse %}
{% for note in notes %}
  <li>
    <span class="item-meta">
      {% if note.date %}<time datetime="{{ note.date | date: '%Y-%m-%d' }}">{{ note.date | date: '%d.%m.%Y' }}</time>{% endif %}
    </span>
    <a class="item-title" href="{{ note.url | relative_url }}">{{ note.title }}</a>
  </li>
{% endfor %}
</ul>
