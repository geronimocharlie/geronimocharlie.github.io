---
layout: page
title: Poetry
permalink: /poetry/
---
<ul class="post-list">
  {% assign items = site.poetry | sort: 'date' | reverse %}
  {% for item in items %}
    <li>
      <a class="post-link" href="{{ item.url | relative_url }}">{{ item.title }}</a>
      <span class="post-meta">
        {% include season_label.html date=item.date label=item.display_date %}
      </span>
      {% if item.location %}
        <span class="post-location"> · {{ item.location }}</span>
      {% endif %}
    </li>
  {% endfor %}
</ul>
