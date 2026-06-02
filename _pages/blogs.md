---
title: "Blogs"
layout: default
excerpt: "Blogs"
sitemap: false
permalink: /blogs/
---

<h1>{{ page.title }}</h1>

<div class="blog-list" style="margin-top: 30px;">
  {% assign sorted_blogs = site.blogs | sort: 'date' | reverse %}
  {% if sorted_blogs.size > 0 %}
    {% for post in sorted_blogs %}
      <div class="blog-post-item" style="margin-bottom: 35px; padding-bottom: 25px; border-bottom: 1px dashed #ddd;">
        <h3 style="margin-top: 0; margin-bottom: 8px; font-weight: 600;">
          <a href="{{ post.url | prepend: site.baseurl }}" style="color: #2c3e50; text-decoration: none;">{{ post.title }}</a>
        </h3>
        
        <div class="blog-post-meta" style="color: #7f8c8d; font-size: 0.9em; margin-bottom: 12px;">
          <span><i class="far fa-calendar-alt" aria-hidden="true"></i> {{ post.date | date: "%B %-d, %Y" }}</span>
          {% if post.categories and post.categories != empty %}
            <span style="margin-left: 15px;"><i class="fas fa-tags" aria-hidden="true"></i> 
            {% for category in post.categories %}
              <span class="label label-info text-capitalize">{{ category }}</span>{% unless forloop.last %} {% endunless %}
            {% endfor %}
            </span>
          {% endif %}
        </div>
        
        <div class="blog-post-excerpt" style="color: #555; line-height: 1.6;">
          {% if post.excerpt %}
            {{ post.excerpt | strip_html | truncatewords: 60 }}
          {% else %}
            {{ post.content | strip_html | truncatewords: 60 }}
          {% endif %}
        </div>
        
        <div style="margin-top: 10px;">
          <a href="{{ post.url | prepend: site.baseurl }}" class="btn btn-default btn-xs" style="border-radius: 4px;">Read More <i class="fas fa-chevron-right" aria-hidden="true" style="font-size: 0.8em;"></i></a>
        </div>
      </div>
    {% endfor %}
  {% else %}
    <p class="text-muted">No blog posts found.</p>
  {% endif %}
</div>
