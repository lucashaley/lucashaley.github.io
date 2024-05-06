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

{% if post.splash_image %}
![]({{ post.splash_image | relative_url }})
{% endif %}

{% if post.excerpt %}
{{ post.excerpt }}
{% endif %}

[Read more]({{ site.baseurl }}{{ post.url }})

{% endfor %}