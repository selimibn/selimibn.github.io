---
layout: page
permalink: /notas/
title: notas
description: Notas de mis cursos
---

<ul class="post-list">
{% for note in site.notes reversed %}
    <li>
        <h2><a class="note-title" href="{{ note.url | prepend: site.baseurl }}">{{ note.title }}</a></h2>
        <p class="post-meta">{{ note.date | date: '%B %-d, %Y — %H:%M' }}</p>
        <p>{{ note.description }}</p>
        <br/>
        <hr/>
      </li>
{% endfor %}
</ul>
