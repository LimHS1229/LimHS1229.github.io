---
layout: page
title: About Me
permalink: /About_Me/
---

<div class="aboutme-embed">
  <iframe
    src="/AboutmeLHS.github.io/"
    title="About Me"
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade"></iframe>
</div>

<p>
  If the embedded page does not load, open
  <a href="/AboutmeLHS.github.io/">About Me</a>.
</p>

<section class="aboutme-recent-posts">
  <h2>Recent Posts</h2>
  {% assign recent_posts = site.posts | sort: "date" | reverse %}
  {% if recent_posts.size > 0 %}
  <ul class="recent-post-list">
    {% for post in recent_posts limit: 5 %}
    <li class="recent-post-item">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
    </li>
    {% endfor %}
  </ul>
  <p class="recent-posts-more">
    <a href="{{ '/posts/' | relative_url }}">See all posts</a>
  </p>
  {% else %}
  <p>No posts have been published yet.</p>
  {% endif %}
</section>

<style>
  body {
    background: #f2f2f2;
  }
  main,
  .page-content {
    background: #f2f2f2;
  }
  .aboutme-embed {
    width: 140%;
    margin: 1rem 0 0.5rem;
  }
  .aboutme-embed iframe {
    width: 100%;
    min-height: 85vh;
    border: 0;
    border-radius: 10px;
    background: #f2f2f2;
  }
  .aboutme-recent-posts {
    margin: 1.5rem 0 0.5rem;
    padding: 1rem 1.1rem;
    border-radius: 10px;
    background: #ffffff;
  }
  .aboutme-recent-posts h2 {
    margin-top: 0;
    margin-bottom: 0.75rem;
  }
  .recent-post-list {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .recent-post-item {
    display: flex;
    justify-content: space-between;
    gap: 1rem;
    align-items: baseline;
    padding: 0.55rem 0;
    border-bottom: 1px solid #e3e3e3;
  }
  .recent-post-item:last-child {
    border-bottom: 0;
  }
  .recent-post-item time {
    color: #666666;
    font-size: 0.9rem;
    white-space: nowrap;
  }
  .recent-posts-more {
    margin: 0.8rem 0 0;
  }
  @media (max-width: 768px) {
    .aboutme-embed {
      width: 100%;
    }
    .recent-post-item {
      flex-direction: column;
      gap: 0.2rem;
      align-items: flex-start;
    }
  }

  /* Keep current light mode, but follow Hydejack dark palette in dark mode */
  body.dark-mode {
    background: var(--body-bg);
  }
  body.dark-mode main,
  body.dark-mode .page-content {
    background: var(--body-bg);
  }
  body.dark-mode .aboutme-embed iframe {
    background: var(--body-bg);
  }
  body.dark-mode .aboutme-recent-posts {
    background: var(--gray-bg);
    border: 1px solid var(--border-color);
  }
  body.dark-mode .recent-post-item {
    border-bottom: 1px solid var(--border-color);
  }
  body.dark-mode .recent-post-item time {
    color: var(--gray-text);
  }

  @media (prefers-color-scheme: dark) {
    body:not(.light-mode) {
      background: var(--body-bg);
    }
    body:not(.light-mode) main,
    body:not(.light-mode) .page-content {
      background: var(--body-bg);
    }
    body:not(.light-mode) .aboutme-embed iframe {
      background: var(--body-bg);
    }
    body:not(.light-mode) .aboutme-recent-posts {
      background: var(--gray-bg);
      border: 1px solid var(--border-color);
    }
    body:not(.light-mode) .recent-post-item {
      border-bottom: 1px solid var(--border-color);
    }
    body:not(.light-mode) .recent-post-item time {
      color: var(--gray-text);
    }
  }
</style>
