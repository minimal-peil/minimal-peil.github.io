---
layout: home
description: ミニマリズムとパーマカルチャー、そして日々の気づきを綴るブログ。
---

小さくて豊かな日々の記録。Minimal Peil は、  
ミニマリズム・パーマカルチャー・ジャズをやさしくつなぐ暮らしの記録です🌿

👤 [About(プロフィール)](profile.md)

---

## 🌱 最新記事一覧

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | markdownify }}

[続きを読む]({{ post.url }})

---

{% endfor %}
