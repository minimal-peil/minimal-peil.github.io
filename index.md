---
layout: default
---

<h1>最新記事</h1>

{% assign counter = 0 %}
{% for post in site.posts %}
  <div class="post-card {% if counter == 0 %}latest{% endif %}">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

    {% if counter == 0 %}
      <div class="post-content">{{ post.content }}</div>
    {% else %}
      <div class="post-excerpt">{{ post.excerpt | markdownify }}</div>
      <a class="read-more" href="{{ post.url }}">続きを読む →</a>
    {% endif %}
  </div>
  {% assign counter = counter | plus: 1 %}
  {% if counter > 3 %}
    {% break %}
  {% endif %}
{% endfor %}
