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

<style>
  .aboutme-embed {
    --embed-width: min(1700px, calc(100vw - 0.5rem));
    position: relative;
    width: var(--embed-width);
    left: calc(100% - var(--embed-width));
    margin: 1rem 0 0.5rem;
  }
  .aboutme-embed iframe {
    display: block;
    width: 100%;
    min-height: 85vh;
    border: 0;
    border-radius: 10px;
    background: #fff;
  }
</style>
