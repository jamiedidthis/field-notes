---
layout: page
title: Books
permalink: /books/
pagination: 
  enabled: true
  category: books
  per_page: 24
  permalink: '/:num/'
  collection: notes
---

<h1>Library<span class="color-subtext">/Anti-library</span></h1>

<p>It’s meant to all overlap in unexpected ways and spark surprises. There are links and annotations galore. So start with what piques your interest, there are no wrong paths to follow.</p>

{% assign booklist = paginator.posts | last_modified_date_source: false %}
{% include booklist.html %}

  {% include pagination.html %}