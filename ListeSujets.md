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

      <span class="post-meta">{{ post.ID }}</span>

      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }} </a>
      </h2>
       {{ post.encadrant }}
    </li>
  {% endfor %}
</ul>

</div>
</body>
