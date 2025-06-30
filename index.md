{% assign counter = 0 %}

{% for post in site.posts %}
  {% if counter == 0 %}
  <!-- 最新記事（1つだけ全文表示） -->
  ### [{{ post.title }}]({{ post.url }})
  
  {{ post.content }}

  ---
  {% else %}
  <!-- 2つ目以降（抜粋＋続きを読む） -->
  ### [{{ post.title }}]({{ post.url }})

  {{ post.excerpt | markdownify }}

  [続きを読む]({{ post.url }})

  ---
  {% endif %}
  
  {% assign counter = counter | plus: 1 %}
{% endfor %}
