---
layout: page
title: Blog
permalink: /blog/
---

<div class="page-title">
    {{page.title}}
</div>

<div class="site-nav-sub">
    <span class = "site-nav-sub-item">
        [<a class="page-link" href="{{sitePage.url}}\blog\programming">programming</a>]
    </span>
    <span class = "site-nav-sub-item">
        [<a class="page-link" href="{{sitePage.url}}\blog\books">books</a>]
    </span>
</div>

{% for post in site.posts %}
    {% include list-posts.html %}
{% endfor %}
