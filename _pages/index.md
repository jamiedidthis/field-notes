---
layout: page
title: Home
id: home
permalink: /
---

## Hello! I read [[books]], I write [[notes]], and here is where I collect, connect, and cross-pollinate their ideas.

<hr>
  <div class="library">
  <h3><a class="internal-link" href="/books">Library &#8594;</a></h3>
  {% assign booklist = site.notes | where: "category", "books" | last_modified_date_sort: false %}
<div id="books">
    {% for book in booklist limit:4 %}
      <div class="book-entry">
        <div class="book-image">
          <a class="internal-link" href="/books/{{ book.title | slugify }}"><img class="book-img" src="/assets/book-covers/{{ book.cover }}" alt="book cover for {{ page.title }}"></a>
        </div>
          <p><a class="internal-link internal-link-unstyled" href="/books/{{ book.title | slugify }}"><em>{{ book.title }}</em></a></p>
          <p class="sans"><a class="internal-link internal-link-unstyled" href="/authors/{{ book.author | slugify }}">{{ book.author }}</a>{% if book.coauthor %}, <a class="internal-link internal-link-unstyled" href="/authors/{{ book.coauthor | slugify }}">{{ book.coauthor }}</a>{% endif %}</p>
      </div>
    {% endfor %}
    </div>
  </div>

  <hr>

<h3><a class="internal-link" href="/notes">Notes &#8594;</a></h3>

<h3><a class="internal-link" href="/Tags">Tags &#8594;</a></h3>

{% include button.html buttonLabel="See latest &#8594;" destinationURL="changelog" %}

<style>

  h3 {
    margin-top: 0;
  }

  h3 .internal-link {
    text-decoration: none;
  }

  #backlinks {
    border-top: 0;
  }