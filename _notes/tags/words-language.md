---
layout: page
title: Words + Language
permalink: /tags/:slug
pagination: 
  enabled: true
  tags: "Words + Language"
  per_page: 24
  permalink: '/:num/'
  collection: notes
---

<h1>{{ page.title }}</h1>

<p>It’s meant to all overlap in unexpected ways and spark surprises. There are links and annotations galore. So start with what piques your interest, there are no wrong paths to follow.</p>

{% assign bookList = paginator.posts | last_modified_date_source: false %}
<div id="books">
  {% for book in bookList %}
    <div class="book-entry">
      <div class="book-image">
        <a class="internal-link" href="/books/{{ book.title | slugify }}"><img class="book-img" src="/assets/book-covers/{{ book.cover }}" alt="book cover for {{ page.title }}"></a>
      </div>
        <p><a class="internal-link internal-link-unstyled" href="/books/{{ book.title | slugify }}"><em>{{ book.title }}</em></a></p>
        <p class="sans"><a class="internal-link internal-link-unstyled" href="/authors/{{ book.author | slugify }}">{{ book.author }}</a>{% if book.coauthor %}, <a class="internal-link internal-link-unstyled" href="/authors/{{ book.coauthor | slugify }}">{{ book.coauthor }}</a>{% endif %}</p>
    </div>
  {% endfor %}
  </div>

  {% include pagination.html %}