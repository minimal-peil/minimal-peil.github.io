{% assign counter = 0 %}

{% for post in site.posts %}
  <div class="post-card {% if counter == 0 %}latest{% endif %}">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

{% assign counter = 0 %}

{% for post in site.posts %}
  <div class="post-card {% if counter == 0 %}latest{% endif %}">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

    {% if counter == 0 %}
      <!-- 最新記事：全文表示 -->
      <div class="post-content">{{ post.content }}</div>
    {% else %}
      <!-- 2〜4番目：抜粋＋続きを読む -->
      <div class="post-excerpt">{{ post.excerpt | markdownify }}</div>
      <a class="read-more" href="{{ post.url }}">続きを読む →</a>
    {% endif %}
  </div>

  {% assign counter = counter | plus: 1 %}
  {% if counter > 3 %}
    {% break %}
  {% endif %}
{% endfor %}

{% if site.posts.size > 4 %}
  <div class="pagination">
    <a href="/page2.md">次のページ →</a>
  </div>
{% endif %}
