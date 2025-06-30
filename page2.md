{% assign counter = 0 %}

{% for post in site.posts offset:4 %}
  ### [{{ post.title }}]({{ post.url }})

  {{ post.excerpt | markdownify }}

  [続きを読む]({{ post.url }})

  ---
{% endfor %}

[← トップページに戻る](/)
