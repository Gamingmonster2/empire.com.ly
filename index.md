---
layout: home
---

<div class="posts-container">
  {% for post in site.posts %}
    <div class="glass-card">
      <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">قراءة المقال &larr;</a>
    </div>
  {% endfor %}
</div>

<style>
  .posts-container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 30px;
  }
  .glass-card {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 12px;
    padding: 24px;
    transition: transform 0.3s ease, border-color 0.3s ease;
  }
  .glass-card:hover {
    transform: translateY(-3px);
    border-color: rgba(255, 255, 255, 0.3);
  }
  .post-date {
    font-size: 0.85rem;
    color: #888;
    display: block;
    margin-bottom: 8px;
  }
  .glass-card h2 {
    margin: 0 0 12px 0;
    font-size: 1.4rem;
  }
  .glass-card h2 a {
    text-decoration: none;
    color: inherit;
  }
  .glass-card p {
    color: #aaa;
    font-size: 0.95rem;
    line-height: 1.6;
    margin-bottom: 15px;
  }
  .read-more {
    font-size: 0.9rem;
    text-decoration: none;
    color: #3b82f6;
    font-weight: bold;
  }
</style>
