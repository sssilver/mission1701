---
layout: default
---

{% for post in site.posts %}
<article>
  <time>{{ post.date | date: "%B %-d, %Y. %A. %H:%M." }}</time>
  {% if post.title %}<h1>{{ post.title }}</h1>{% endif %}
  {{ post }}
</article>
{% endfor %}
