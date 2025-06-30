{% assign counter = 0 %}

{% for post in paginator.posts %}
  {% if counter == 0 %}
  <!-- 最新記事だけ全文表示 -->
  ### [{{ post.title }}]({{ post.url }})

  {{ post.content }}

  ---
  {% elsif counter <= 3 %}
  <!-- 2〜4番目の記事は抜粋だけ -->
  ### [{{ post.title }}]({{ post.url }})

  {{ post.excerpt | markdownify }}

  [続きを読む]({{ post.url }})

  ---
  {% endif %}

  {% assign counter = counter | plus: 1 %}
{% endfor %}

<!-- ページネーションリンク -->
{% if paginator.previous_page %}
[← 前のページ]({{ paginator.previous_page_path }})
{% endif %}

{% if paginator.next_page %}
[次のページ →]({{ paginator.next_page_path }})
{% endif %}
