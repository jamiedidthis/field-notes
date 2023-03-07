---
layout: page
title: Publishers
permalink: /publishers
---

# Publishers
<ul>
  {% for publisher in site.publishers %}
    <li><a class="internal-link internal-link-unstyled" href="/publishers/{{ publisher.title | slugify }}">{{ publisher.title }}</a></li>
  {% endfor %}
</ul>



<style>
    #books {
      display: grid;
      grid-template-columns: repeat(auto-fill, 148px);  
      grid-gap: 2rem;
      justify-content: center;
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
      height: 225px;
      margin: 0 0 15px 0;
    }

    #books img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    h2:first-of-type {
      margin-top: 3rem;
    }


</style>