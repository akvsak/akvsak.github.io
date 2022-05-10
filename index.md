---
title: AK's Homepage
--- 

### Links

### Blog Posts 

{% for post in site.posts %}
{% unless post.categories contains "now" %}

[{{ post.title }}]({{ post.url }}) {{ post.date | date: "%Y-%m-%d" }}

{% endunless %}
{% endfor %}

### Other links

[random post page](/random) || [dynamic now page](/now) || [tag page](/tags) || [category page](/categories) [blog design](/dev)
