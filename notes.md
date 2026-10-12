---
layout: default
title: Заметки
permalink: /notes/
---

# Заметки

<p class="lede">Материалы и конспекты обсуждений клуба.</p>

<ul class="item-list">
{% assign notes = site.notes | sort: 'date' | reverse %}
{% for note in notes %}
  <li>
    <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
    <span class="item-meta">
      {% if note.date %}<time datetime="{{ note.date | date: '%Y-%m-%d' }}">{{ note.date | date: '%d.%m.%Y' }}</time>{% endif %}
    </span>
  </li>
{% endfor %}
</ul>
