---
layout: page
title: Maya Python
permalink: /MayaPython/
---

{% assign maya_python_posts = site.posts | where_exp: "post", "post.path contains 'MayaPython/_posts/'" | sort: "date" | reverse %}

{% if maya_python_posts.size > 0 %}
{% for post in maya_python_posts %}
<article id="post-{{ post.slug | default: post.title | slugify }}" class="page post mb6" role="article">
  <header>
    <h1 class="post-title flip-project-title">
      <a href="{{ post.url | relative_url }}" class="flip-title">
        {{ post.title | default: post.slug }}
      </a>
    </h1>

    <div class="post-date">
      <span class="ellipsis mr1">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b %Y" }}</time>
      </span>
    </div>

    {% if post.description %}
    <p class="note-sm">
      {{ post.description }}
    </p>
    {% endif %}
  </header>

  {{ post.excerpt }}

  <footer>
    <p class="read-more">
      Continue reading <a class="heading flip-title" href="{{ post.url | relative_url }}">{{ post.title | default: post.slug }}</a>
    </p>
  </footer>
</article>
{% endfor %}
{% else %}
No posts found in `MayaPython/_posts`.
{% endif %}
