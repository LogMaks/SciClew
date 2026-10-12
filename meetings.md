---
layout: default
title: Встречи
permalink: /meetings/
---

# Встречи

<p class="page-lede">Собрания клуба по датам: тема, повестка и итоги при наличии.</p>

<ul class="item-list">
{% assign meetings = site.meetings | sort: 'date' | reverse %}
{% for meeting in meetings %}
  <li>
    <span class="item-meta">
      {% if meeting.date %}<time datetime="{{ meeting.date | date: '%Y-%m-%d' }}">{{ meeting.date | date: '%d.%m.%Y' }}</time>{% endif %}
      {% if meeting.topic %} · {{ meeting.topic }}{% endif %}
    </span>
    <a class="item-title" href="{{ meeting.url | relative_url }}">{{ meeting.title }}</a>
  </li>
{% endfor %}
</ul>
