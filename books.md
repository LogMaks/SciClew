---
layout: default
title: Книги
permalink: /books/
---

# Книги

<p class="lede">Интересные источники: внешние ссылки и материалы, сохранённые на сайте.</p>

<ul class="item-list">
{% assign books = site.books | sort: 'title' %}
{% for book in books %}
  <li>
    <a href="{{ book.url | relative_url }}">{{ book.title }}</a>
    <span class="item-meta">
      {% if book.author %}{{ book.author }}{% endif %}
      {% if book.kind == 'link' %} · внешняя ссылка{% elsif book.kind == 'onsite' %} · на сайте{% endif %}
    </span>
  </li>
{% endfor %}
</ul>
