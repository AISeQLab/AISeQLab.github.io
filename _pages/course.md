---
title: "Course"
layout: default
excerpt: "Course"
sitemap: false
permalink: /course/
---
<style>
.course-card {
  max-width: 600px;
  border: 1px solid #eee;
  margin: 20px auto;
}

.course-description {
  background-color: #f6f6f6;
  padding: 20px;
  display: flex;
  align-items: flex-start;
  gap: 15px;
}

.course-icon {
  font-size: 28px;
  color: #f7941d;
  flex-shrink: 0;
}

.course-text h3 {
  margin-top: 0;
  margin-bottom: 10px;
}

.course-text p {
  margin: 0;
  line-height: 1.5;
  color: #555;
}

.course-footer {
  background-color: black;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  flex-wrap: wrap;
}

.course-price {
  color: orange;
  font-weight: bold;
  font-size: 18px;
}

.course-price del {
  color: white;
  font-size: 16px;
  margin-left: 5px;
}

.course-duration {
  font-size: 14px;
  display: block;
  margin-top: 5px;
}

.course-btn {
  background-color: white;
  color: black;
  padding: 10px 20px;
  text-decoration: none;
  font-weight: bold;
  margin-top: 10px;
}

@media (max-width: 480px) {
  .course-description {
    flex-direction: column;
  }

  .course-footer {
    flex-direction: column;
    align-items: flex-start;
  }

  .course-btn {
    width: 100%;
    text-align: center;
  }
}
</style>
# Courses [{{ site.data.courses | size }}]

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
