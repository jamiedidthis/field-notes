---
layout: page
title: Books
permalink: /books
---

# Library<span class="color-subtext">/Anti-library</span>

It’s meant to all overlap in unexpected ways and spark surprises. There are links and annotations galore. So start with what piques your interest, there are no wrong paths to follow.

{% assign bookList = site.books | where: "collection", "books" | last_modified_date_sort: false %}
<div id="books">
  {% for book in bookList %}
    <div class="book-entry">
      <div class="book-image">
        <a class="internal-link" href="/books/{{ book.title | slugify }}"><img class="book-img" src="/assets/book-covers/{{ book.cover }}" alt="book cover for {{ page.title }}"></a>
      </div>
        <p><a class="internal-link internal-link-unstyled" href="/books/{{ book.title | slugify }}"><em>{{ book.title }}</em></a></p>
        <p class="sans"><a class="internal-link internal-link-unstyled" href="/authors/{{ book.written_by | slugify }}">{{ book.written_by }}</a>{% if book.coauthor %}, <a class="internal-link internal-link-unstyled" href="/authors/{{ book.coauthor | slugify }}">{{ book.coauthor }}</a>{% endif %}</p>
    </div>
  {% endfor %}
  </div>
