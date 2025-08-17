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

# Project (Gen 1)

Check the [link](https://docs.google.com/spreadsheets/d/1gswsvpBxHxGYJV5gXpZ4qD-7IA735JHvY7n1P2ABLPI/edit?usp=sharing) for list of existing projects:

<div style="width:100%;overflow-x:auto;">
    <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQDKL9WtVNjzYffCQQe9037VuR2ILXGXg9HRn5lT6ad0Ng3IiEyUpfOEoA42eFnTE7K9HduPG6oD66q/pubhtml?widget=true&amp;headers=false" width="100%" height="600" frameborder="0"></iframe>
</div>

Check the [link](https://docs.google.com/spreadsheets/d/1vrbcvRWvCJI2dvyBgF6bYcGPCktQ7GpC1CKx0sXq1OQ/edit?usp=sharing) for list of members.