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

# Project

Will be update soon ...