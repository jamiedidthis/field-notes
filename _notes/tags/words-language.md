---
layout: page
title: Words + Language
permalink: /tags/words-language
---

<h1>{{ page.title }}</h1>

<p>It’s meant to all overlap in unexpected ways and spark surprises. There are links and annotations galore. So start with what piques your interest, there are no wrong paths to follow.</p>

{% assign booklist = site.notes | where: "category", "books" | where: "tag", "Words + Language" | last_modified_date_source: false %}
{% include booklist.html %}

{% assign linklist = site.notes | where: "category", "notes" | where: "tag", "Words + Language" | last_modified_date_source: false %}
{% include linklist.html %}