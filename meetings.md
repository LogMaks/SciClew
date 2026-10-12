---
layout: default
title: Встречи
permalink: /meetings/
---

# Встречи

<p class="lede">Собрания клуба по датам: тема, повестка и итоги при наличии.</p>

<ul class="item-list">
{% assign meetings = site.meetings | sort: 'date' | reverse %}
{% for meeting in meetings %}
  <li>
    <a href="{{ meeting.url | relative_url }}">{{ meeting.title }}</a>
    <span class="item-meta">
      {% if meeting.date %}<time datetime="{{ meeting.date | date: '%Y-%m-%d' }}">{{ meeting.date | date: '%d.%m.%Y' }}</time>{% endif %}
      {% if meeting.topic %} · {{ meeting.topic }}{% endif %}
    </span>
  </li>
{% endfor %}
</ul>
