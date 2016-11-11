---
layout: page
title: Projects
permalink: /projects/
---

<div class="page-title">
    {{page.title}}
</div>

<div class="site-nav-sub">
    <span class = "site-nav-sub-item">
        [<a class="page-link" href="{{sitePage.url}}\projects\academic">academic</a>]
    </span>
    <span class = "site-nav-sub-item">
        [<a class="page-link" href="{{sitePage.url}}\projects\personal">personal</a>]
    </span>
</div>

{% for post in site.posts %}
    {% include list-posts.html %}
{% endfor %}
