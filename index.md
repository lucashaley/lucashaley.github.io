---
title: Home
layout: home
nav_order: 1
---

# Lucas Haley

## Recent Posts

{% for post in site.posts limit:3 %}
### {{ post.title }}
#### {{ post.date | date: "%B %e, %Y" }}

{% if post.excerpt %}
{{ post.excerpt }}
{% endif %}

  <article class="post" display="block">
    <a href="{{ site.baseurl }}{{ post.url }}">
      <h2>{{ post.title }}</h2>

      <div>
        <p class="post_date">{{ post.date | date: "%B %e, %Y" }}</p>
      </div>

      {% if post.splash_image %}
      <img class="splash" src="{{ post.splash_image | relative_url }}">
      {% endif %}

    </a>
    {% if post.excerpt %}
    <div class="entry">
      {{ post.excerpt }}
    </div>
    {% endif %}

    <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
  </article>
{% endfor %}