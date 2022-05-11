---
title: AK's Homepage
--- 
### Notes & Posts

{% for post in site.posts %}
{% unless post.categories contains "now" %}

[{{ post.title }}]({{ post.url }}) {{ post.date | date: "%Y-%m-%d" }}

{% endunless %}
{% endfor %}

### Other links

[random post](/random) || [dynamic now page](/now) || [tags](/tags) || [categories](/categories) [blog design](/dev)
