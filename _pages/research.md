---
title: "Research"
layout: default
excerpt: "Research"
sitemap: false
permalink: /research/
---



# Grant [{{ site.data.grants | size }}]
<ul class="list-unstyled">
    {% for grant in site.data.grants %}
        <li class="media">
            <div class="media-body">
            <h4 class="mt-0 mb-1">
                <a href="{{ grant.link }}">{{ grant.title }}</a> [{{ grant.duration }}]
            </h4>
            <p>Amount: {{ grant.amount }}</p>
            {{ grant.content }}
            </div>
        </li>
    {% endfor %}
</ul>

# Tutorials

[High-bandwidth memory usage](https://github.com/AISeQLab/HBM_Tutorial/blob/main/HBM_Tutorial_Markdown/HIGH%20BANDWIDTH%20MEMORY%20(HBM)%202548ba96de7f8077bdb9ccb8f0f1ab4f.md)

# Project (Gen 1)

[List of existing projects](https://docs.google.com/spreadsheets/d/1gswsvpBxHxGYJV5gXpZ4qD-7IA735JHvY7n1P2ABLPI/edit?usp=sharing)

[List of members](https://docs.google.com/spreadsheets/d/1vrbcvRWvCJI2dvyBgF6bYcGPCktQ7GpC1CKx0sXq1OQ/edit?usp=sharing)