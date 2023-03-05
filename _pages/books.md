---
layout: page
title: Books
permalink: /books
---

# Books

{% assign bookList = site.books | where: "collection", "books" | last_modified_date_sort: false %}
<div id="books">
  {% for book in bookList %}
    <div class="book-entry">
      <div class="book-image">
        <a class="internal-link" href="/books/{{ book.title | slugify }}"><img class="book-img" src="/assets/book-covers/{{ book.cover }}" alt="book cover for {{ page.title }}"></a>
      </div>
        <p><a class="internal-link internal-link-unstyled" href="/books/{{ book.title | slugify }}"><em>{{ book.title }}</em></a></p>
        <p class="sans"><a class="internal-link internal-link-unstyled" href="/books/{{ book.author_slug }}">{{ book.author }}</a></p>
    </div>
  {% endfor %}
  </div>

<style>
    #books {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
      padding-left: 0;
      grid-gap: 2rem;
      list-style-type: none;
    }

    @media screen and (max-width: 760px) {
      #books {
        grid-template-columns: 1fr 1fr;
        grid-gap: 1rem;
      }
    }

    #books p { 
      font-size: 0.9em;
      line-height: 1.2em;
      margin: 5px 0 0 0;
      padding: 0;
    }

    #books p.sans {
      font-size: 0.7em;
      line-height: 1em;
    }

    #books .book-entry a {
        border-bottom: none;
        background-color: transparent;
        text-decoration: none;
    }

    div.book-image {

    }

     #books img {
      max-width: 400px;
      width:100%;
      object-fit: cover;
    }

    #books div {
      line-height: 1.2;
    }

    @media screen and (max-width: 600px) {
      h1 {
          margin-left: auto;
          text-align: center;
      }

      h2 {
          text-align: center;
      }
    }

    h2:first-of-type {
      margin-top: 3rem;
    }


</style>