---
title: Ashok Kumar's Homepage
--- 

### Links

### Blog Posts 

{% for post in site.posts %}
{% unless post.categories contains "now" %}

[{{ post.title }}]({{ post.url }}){{ post.date }}

{% endunless %}
{% endfor %}


### Other links

[random post page](/random) || [dynamic now page](/now) || [demo tag page](/tags)

### Blog Design Links

[original source code on GitHub](https://github.com/derekkedziora/jekyll-demo) 

[dark mode guide](https://derekkedziora.com/blog/dark-mode-revisited) 

Make sure you have the dark mode toggle on each page, otherwise you'll always display the system color preference.

[Build random post link using client side JS](https://derekkedziora.com/blog/Getting-Random-Post-in-Jekyll) 

[making a tag page](https://derekkedziora.com/blog/tag-page-jekyll).