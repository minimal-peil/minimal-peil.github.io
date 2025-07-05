---
layout: default
description: 小さくて豊かな日々の記録。
ミニマリズム・パーマカルチャー・ジャズをやさしくつなぐ暮らしの記録です🌿
---

[About(プロフィール)](profile.md)

---

{% assign counter = 0 %}

{% for post in site.posts %}
  {% if counter <= 3 %}
  <!-- 最新〜4番目まで（抜粋＋続きを読む） -->
  [{{ post.title }}]({{ post.url }})

  {{ post.excerpt | markdownify }}

  [続きを読む]({{ post.url }})

  ---
  {% endif %}

  {% assign counter = counter | plus: 1 %}
{% endfor %}

{% if site.posts.size > 4 %}
[次のページ →](/page2.md)
{% endif %}
