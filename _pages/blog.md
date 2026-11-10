---
title: "Blog"
layout: modern
permalink: /blog/
---

<div class="post-list">
{% for post in site.posts %}
<section class="post-entry">
<time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
<h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
<p>{{ post.excerpt | strip_html | truncatewords: 38 }}</p>
<a class="read-post" href="{{ post.url | relative_url }}">Read post →</a>
</section>
{% endfor %}
</div>
