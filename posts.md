---
layout: page
title: Posts
permalink: /posts/
---

<div class="posts-archive">
  {% for post in site.posts %}
    <article class="post-archive-item">
      <div class="post-archive-header">
        <time class="post-archive-date" datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%b %-d, %Y" }}
        </time>
        {% if post.tags and post.tags.size > 0 %}
          <div class="post-archive-tags">
            {% for tag in post.tags %}
              <span class="tag">#{{ tag }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
      
      <h2 class="post-archive-title">
        <a href="{{ post.url | relative_url }}" class="post-archive-link">
          {{ post.title }}
        </a>
      </h2>
      
      <div class="post-archive-summary">
        {% if post.summary %}
          {{ post.summary }}
        {% else %}
          {{ post.excerpt | strip_html | truncatewords: 30 }}
        {% endif %}
      </div>
    </article>
  {% endfor %}
</div> 