---
title: Home
layout: default
---

<section class="hero">
  <p class="eyebrow">Affiliate Micro</p>
  <h1>Discover smart tools that can improve your workflow.</h1>
  <p class="lead">
    This site shares practical reviews, honest takeaways, and affiliate recommendations for developers, creators, and growing teams.
  </p>
  <div class="hero-actions">
    <a class="button primary" href="#recent-posts">Explore recent posts</a>
    <a class="button secondary" href="#features">See what’s covered</a>
  </div>
</section>

<section id="features" class="features">
  <div>
    <h2>Useful recommendations</h2>
    <p>Each post highlights what the tool does well, where it falls short, and who it is best for.</p>
  </div>
  <div>
    <h2>Easy to scan</h2>
    <p>The format is built for quick reading, so readers can decide fast whether a tool is worth trying.</p>
  </div>
  <div>
    <h2>Designed to keep publishing</h2>
    <p>Automation and repeatable workflows help the site stay active with fresh content over time.</p>
  </div>
</section>

<section class="featured-posts">
  <div class="section-heading">
    <p class="eyebrow">Featured</p>
    <h2>What’s worth reading</h2>
  </div>

  <div class="featured-grid">
    {% for post in site.posts limit: 3 %}
      <article class="featured-card">
        <p class="card-date">{{ post.date | date: "%B %d, %Y" }}</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
      </article>
    {% endfor %}
  </div>
</section>

<section id="recent-posts" class="recent-posts">
  <div class="section-heading">
    <p class="eyebrow">Latest updates</p>
    <h2>Recent posts</h2>
  </div>

  <ul class="post-list">
    {% for post in site.posts limit: 5 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span>{{ post.date | date: "%B %d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
</section>
