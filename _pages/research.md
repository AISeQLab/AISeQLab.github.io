---
title: "Research"
layout: default
excerpt: "Research"
sitemap: false
permalink: /research/
---

# 

**Grants** {{ site.data.grants | size }}
<ul class="list-unstyled">
    {% for grant in site.data.grants %}
        <li class="media">
            <div class="media-body">
            <h4 class="mt-0 mb-1">
                [{{ grant.duration }}]
                <a href="{{ grant.link }}">{{ grant.title }}</a>
            </h4>     <p>{{ grant.amount }}</p>
            {{ grant.content }}
            </div>
        </li>
    {% endfor %}
</ul>
# Research