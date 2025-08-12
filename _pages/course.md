---
title: "Course"
layout: default
excerpt: "Course"
sitemap: false
permalink: /course/
---

<h1>Courses [{{ site.data.courses | size }}]</h1>

{% for course in site.data.courses %}
<div class="course-card">
  <div class="course-description">
    <div class="course-icon"></div>
    <div class="course-text">
      <h3>{{ course.title }}</h3>
      <p>{{ course.content }}</p>
    </div>
  </div>
  <div class="course-footer">
    <a href="{{ course.link }}" class="course-btn">Start</a>
    <div>
      <span class="course-price">{{ course.price }}</span>
      <span class="course-duration">{{ course.duration }}</span>
    </div>
  </div>
</div>
{% endfor %}
