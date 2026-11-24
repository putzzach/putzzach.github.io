---
layout: page
title: Tags
permalink: /tags/
---

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  {% assign tag_name = tag[0] %}
  {% assign tagged_posts = tag[1] | sort: "date" | reverse %}
<section id="{{ tag_name | slugify }}">
  <h2>{{ tag_name | escape }}</h2>
  <ul>
    {% for post in tagged_posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></li>
    {% endfor %}
  </ul>
</section>
{% endfor %}
