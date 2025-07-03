---
layout: default
---
{% assign counter = 0 %}

{% for post in site.posts %}
  {% if counter == 0 %}
  <!-- 最新記事（全文表示） -->
   [{{ post.title }}]({{ post.url }})

  {{ post.content }}

  ---
  {% elsif counter <= 3 %}
  <!-- 2〜4番目（抜粋＋続きを読む） -->
   [{{ post.title }}]({{ post.url }})

  {{ post.excerpt | markdownify }}

  [続きを読む]({{ post.url }})

  ---
  {% endif %}

  {% assign counter = counter | plus: 1 %}
{% endfor %}

{% if site.posts.size > 4 %}
[次のページ →](/page2.md)
{% endif %
