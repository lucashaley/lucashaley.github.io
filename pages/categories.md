---
title: Categories
nav_order: 4
permalink: /categories/
layout: page
---
<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}

    <h3 class="category-head">{{ category_name }}</h3>

    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h5><a href="{{ site.baseurl }}{{ post.url }}">{% if post.title and post.title != "" %}{{post.title}}{% else %}{{post.excerpt |strip_html}}{%endif%} ({{ post.date | date: "%B %Y" }})</a></h5>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>