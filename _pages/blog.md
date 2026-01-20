---
title: "Blog"
layout: archive
permalink: /blog/
author_profile: true
---

{% for post in site.posts %}
<div class="list__item">
  <article class="archive__item">
    <h2 class="archive__item-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="page__meta">{{ post.date | date: "%B %d, %Y" }}</p>
  </article>
</div>
{% endfor %}

