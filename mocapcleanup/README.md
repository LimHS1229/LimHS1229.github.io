---
layout: page
title: MocapClean
permalink: /mocapcleanup/
---

{% assign mocap_posts = site.posts | where_exp: "post", "post.path contains 'mocapcleanup/_posts/'" | sort: "date" | reverse %}

{% if mocap_posts.size > 0 %}
{% for post in mocap_posts %}
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

    {% if post.image and post.image.path %}
    <a href="{{ post.url | relative_url }}" class="no-hover no-print-link flip-project" tabindex="-1">
      <div class="img-wrapper lead aspect-ratio sixteen-nine flip-project-img">
        <img
          src="{{ post.image.path | relative_url }}"
          {% if post.image.srcset %}srcset="{% for item in post.image.srcset %}{{ item[1] | relative_url }} {{ item[0] }}{% unless forloop.last %},{% endunless %}{% endfor %}"{% endif %}
          alt="{{ post.title | default: post.slug }}"
          loading="lazy"
        />
      </div>
    </a>
    {% endif %}

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
No posts found in `mocapcleanup/_posts`.
{% endif %}
