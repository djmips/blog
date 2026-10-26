---
layout: default
---

Notes from a game programmer.

{% assign posts = site.pages | where_exp: "p", "p.date" | sort: "date" | reverse %}
<ul class="posts">
{% for p in posts %}<li><span class="date">{{ p.date | date: "%-d %b %Y" }}</span> <a href="{{ p.url | relative_url }}">{{ p.title }}</a><br><span class="desc">{{ p.description }}</span></li>
{% endfor %}</ul>
