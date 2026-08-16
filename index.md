---
title: Weekly News Recap
---

## All recaps

{% assign recap_pages = site.pages | where_exp: "p", "p.path contains 'posts/'" | sort: "path" | reverse %}
{% for p in recap_pages %}
- [{{ p.name | remove: ".md" }}]({{ p.url | relative_url }})
{% endfor %}
