---
layout: page
title: Series
permalink: /series
---

# Series

<div class="container">
<ul>
  {% assign series = site.notes | where: "category", "series" %}
  {% for series in series %}
    <li><a class="internal-link" href="/series/{{ series.title | slugify }}">{{ series.title }}</a></li>
  {% endfor %}
</ul>
</div>


<style>

.container { 
  column-count: 2; 
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