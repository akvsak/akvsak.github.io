---
title: Blog Development Page
--- 

[random post page](/random) || [dynamic now page](/now) || [demo tag page](/tags)

### Blog Design Links

[original source code on GitHub](https://github.com/derekkedziora/jekyll-demo) 

[dark mode guide](https://derekkedziora.com/blog/dark-mode-revisited) 

Make sure you have the dark mode toggle on each page, otherwise you'll always display the system color preference.

[Build random post link using client side JS](https://derekkedziora.com/blog/Getting-Random-Post-in-Jekyll) 

### Tags

[making a tag page](https://derekkedziora.com/blog/tag-page-jekyll)

<div markdown=1 style="min-height: 100vh;">

You can style the tag menu and each tag section with `min-height: 100vh;`

Then add a back to top link at the bottom of each section. This looks less cluttered when you have lot of tags and posts.

Check out my full guide to [making a tag page in Jekyll](https://derekkedziora.com/blog/tag-page-jekyll).


### Now Page
  
Check out my full guide to setting up a [dynamic now page](https://derekkedziora.com/blog/dynamic-now-page).

This page does everything I want: 

- Automatically updates 
- Includes each new "Now" entry in my RSS feed
- Doesn't include now pages on my post list 

Each now post needs to have the category "now" added to the front matter. Otherwise, you can write like a regular post. 

Make sure you add this to your `_config` file. You'll get your now posts in your regular RSS feed (example: [/feed.xml](https://demo.derekkedziora.com/feed.xml) and a second feed with just now posts to boot (example: [/feed/now.xml](https://demo.derekkedziora.com/feed/now.xml))

```
plugins:
  - jekyll-feed

feed: 
  categories: 
  - now
```

The only code on the static `now.md` you need to display the most recent now post is this: 

```
{% raw %}{{ site.categories.now[0].content }}{% endraw %}
```
