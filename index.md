{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | markdownify }}

[続きを読む]({{ post.url }})

---

{% endfor %}
