---
title: "Course"
layout: default
excerpt: "Course"
sitemap: false
permalink: /course/
---
<style>
        .container {
            max-width: 100%;
            padding-left: 0px;
            padding-right: 0px;
        }

        .course-title {
            text-align: left;
            font-weight: 600;
            margin-bottom: 20px
        }

        .course-title::after {
            width: 80px;
            height: 4px;
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
        }

        .module {
            display: flex;
            align-items: flex-start;
            margin-bottom: 5px;
            padding: 20px;
            border: 1px solid #e0e0e0;
            transition: all 0.3s ease;
        }

        .module:hover {
            box-shadow: 0 0px 10px rgba(0, 0, 0, 0.08);
            transform: translateY(-2px);
        }

        .module.expanded {
            background-color: white;
        }


        .module-content {
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .module-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            width: 100%;
        }

        .module-title {
            color: black;
            line-height: 1.4;
            margin-top: 0px;
            margin-bottom: 0px;
            margin-right: 20px;
            padding: 0px
        }

        .module-toggle {
            font-size: 1.5em;
            transition: transform 0.3s ease;
            font-weight: bold;
        }

        .module-toggle.expanded {
            transform: rotate(180deg);
        }

        .module-body {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-in-out;
            padding-top: 0;
            opacity: 0;
        }

        .module-body.expanded {
            max-height: 1000px; /* Adjust as needed */
            padding-top: 20px;
            opacity: 1;
        }

        .module-details {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .module-image-container {
            flex: 1 1 300px;
            overflow: hidden;
        }

        .module-image {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 0px;
        }

        .module-list-container {
            flex: 1 1 300px;
        }
        
        .module-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .module-list li {
            font-size: 1em;
            line-height: 1.6;
            padding: 8px 0;
            border-bottom: 1px dashed #e0e0e0;
            color: #555;
            display: flex;
            align-items: flex-start;
        }
        
        .module-list li:last-child {
            border-bottom: none;
        }

        .module-list li::before {
            font-weight: bold;
            margin-right: 8px;
            flex-shrink: 0;
        }

        .module-list h4 {
            font-size: 1.1em;
            font-weight: 600;
            color: #333;
            margin: 0 0 5px 0;
        }

        .button-register {
              font-size: 18px;
              background: none;
              border: none;
              color: #000;
              position: relative;
              cursor: pointer;
              padding-top: 10px;
              padding-bottom: 10px;
              padding-right: 20px;
              padding-left: 0px;
            }


        .button-register::after {
              content: "";
              position: absolute;
              left: 50%;
              bottom: 0;
              transform: translateX(-50%);
              width: 0%;
              height: 3px;
              background: black; /* green */
              transition: width 0.3s ease-in-out;
              border-radius: 2px;
            }

            /* animate underline on hover */
            .button-register:hover::after {
              width: 100%; /* underline length when hovered */
            }

            /* optional: change text color on hover */
            .button-register:hover {
              color: green;
            }

        html {
            scroll-behavior: smooth;
      }
</style>

<script>
    document.addEventListener('DOMContentLoaded', function() {
        const modules = document.querySelectorAll('.module');
        modules.forEach(module => {
            const header = module.querySelector('.module-header');
            const body = module.querySelector('.module-body');
            const toggle = module.querySelector('.module-toggle');

            header.addEventListener('click', () => {
                const isExpanded = module.classList.contains('expanded');

                // Close any other open modules
                document.querySelectorAll('.module.expanded').forEach(openModule => {
                    if (openModule !== module) {
                        openModule.classList.remove('expanded');
                        openModule.querySelector('.module-body').classList.remove('expanded');
                        openModule.querySelector('.module-toggle').classList.remove('expanded');
                    }
                });

                // Toggle the clicked module
                module.classList.toggle('expanded');
                body.classList.toggle('expanded');
                toggle.classList.toggle('expanded');
            });
        });

        // Auto-expand Module 1 on page load
        const module1 = document.getElementById('module-1');
        if (module1) {
            module1.classList.add('expanded');
            module1.querySelector('.module-body').classList.add('expanded');
            module1.querySelector('.module-toggle').classList.add('expanded');
        }
    });
</script>
# Khoá học
<ul style="margin-left: 0; padding-left: 0;">
    {% for course in site.data.courses %}
    <div class="course-card">
        <div class="course-description">
            <div class="course-icon"></div>
            <div class="course-text">
                <h3>{{ course.title }} [{{ course.duration }}]</h3>
            </div>
        </div>
        <img src="{{ course.image }}" alt="{{ course.title }}" style="width: 100%; display: block; margin-bottom: 20px">
        <div class="course-footer">
            <div>
                <span class="course-price">{{ course.comment }}</span>
            </div>
            <button class="button-register" onclick="document.getElementById('#course{{ forloop.index }}').scrollIntoView({ behavior: 'smooth' })">
            <strong>Chi tiết</strong>
          </button>
          <a class="button-register" href="/register">
            <strong>Đăng ký</strong>
          </a>
        </div>
    </div>
    {% endfor %}
</ul>
<hr/>


<ul style="margin-left: 0; padding-left: 0;">
  {% for course in site.data.courses %}
  <div class="container" id = "#course{{ forloop.index }}">
    <div>
      <h2 class="course-title">[{{forloop.index}}] {{course.title}}</h2>
      {% if course.comment %}
      <p style="margin-bottom: 20px">{{course.comment}}</p>
      {% endif %}
    </div>
    {% for section in course.detail.section %}
    <h3 class="course-title">{{section.title}}</h3>
    {% if section.comment %}
    <p style="margin-bottom: 20px">{{section.comment}}</p>
    {% endif %}
    <div>
      {% for module in section.module %}
      <div class="module" id="module-1">
        <div class="module-content">
          <div class="module-header">
            <div>
              <p class="module-title">{{module.title}}</p>
            </div>
            <div>
              <span class="module-toggle">+</span>
            </div>
          </div>
          <div class="module-body">
            <div class="module-details">
              <div class="module-image-container">
                {% if module.image %}
                <img src="{{ module.image }}" alt="Python concepts" class="module-image">
                {% endif %}    
              </div>
              <div class="module-list-container">
                <ul class="module-list">
                  {% for title in module.moduledetail %}
                  <p><strong>{{ title | split: ':' | first }}</strong>: {{ title | split: ':' | last }}</p>
                  {% endfor %}    
                </ul>
              </div>
            </div>
          </div>    
        </div>
      </div>
      {% endfor %}
    </div>
    {% endfor %}
    <hr/>
  </div>
  {% endfor %}
</ul>