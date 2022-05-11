---
title: Category Page
permalink: /categories
---
<div markdown=1 style="min-height: 100vh;">

{% for category in site.categories %}

[{{ category[0] }}&nbsp;({{ category[1] | size }})](#{{category[0]}})

{% endfor %}

</div>


{% for category in site.categories %}

<div markdown=1 style="min-height: 100vh;">

## {{category[0]}}

{% for post in category[1] %}

[{{ post.title }}]({{ post.url }})

{% endfor %}

[All categories &#8593;](#)

</div>

{% endfor %}
