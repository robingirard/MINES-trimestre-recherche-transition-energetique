---
layout: default
title: Liste des sujets proposés
---
<body>
<div class="home">

<p>

</p>
Liste des sujets du trimestre recherche
<p>

</p>

{{ content }}

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      {% assign nom_sujet = site.minima.date_format | default: "%b %-d, %Y" %}
      {% assign date_english = post.date | date: date_format %}
      {% include date-french.html %}

      <span class="post-meta">{{ date_french }}</span>

      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }} </a>
      </h2>
       {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

</div>
</body>
