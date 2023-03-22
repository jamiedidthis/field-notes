---
layout: page
title: Publishers
permalink: /publishers
---

# Publishers

<div class="container">
<ul>
  {% assign publishers = site.notes | where: "category", "publishers" %}
  {% for publisher in publishers %}
    <li><a class="internal-link" href="/publishers/{{ publisher.title | slugify }}">{{ publisher.title }}</a></li>
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