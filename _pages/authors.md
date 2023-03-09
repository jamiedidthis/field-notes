---
layout: page
title: Authors
permalink: /authors
---

# Authors

<div class="container">
<ul>
{% assign authors = site.notes | where: "category", "authors" %}
  {% for author in authors %}
    <li><a class="internal-link" href="/authors/{{ author.title | slugify }}">{{ author.title }}</a></li>
  {% endfor %}
</ul>
</div>


<style>

.container { 
  column-count: 3; 
  column-width: 215px;
  column-gap: 1em; 
  margin: 2em 0;
}

ul { 
  list-style: none; 
  padding-left: 0;
  margin: 0;
}

</style>