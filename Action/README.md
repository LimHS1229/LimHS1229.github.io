---
layout: page
title: Action
permalink: /Action/
---

## Action Posts

{% assign action_posts = site.posts | where_exp: "post", "post.path | downcase contains 'action/_posts/'" | sort: "date" | reverse %}

{% if action_posts.size > 0 %}
{% for post in action_posts %}
- [{{ post.title | default: post.slug }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
{% else %}
{% assign action_pages = site.pages | where_exp: "page", "page.path | downcase contains 'action/_posts/'" | sort: "path" | reverse %}
{% if action_pages.size > 0 %}
{% for page in action_pages %}
- [{{ page.title | default: page.name }}]({{ page.url | relative_url }})
{% endfor %}
{% else %}
- No posts found in `Action/_posts`.
{% endif %}
{% endif %}