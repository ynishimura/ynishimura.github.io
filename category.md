---
layout: default
title: Category
permalink: /category/
---

<div class="content well">
<header id="post-header">
    <h1 id="post-subtitle">Category Search <em class="text-muted">{{ page.categories }}</em></h1>
</header>

<div id="post-content">
    <hr />
    {% for category in site.categories %}
        {% capture category_slug %}{{ category | first }}{% endcapture %}
        {% for c_slug in category_slug %}
            {% if c_slug == page.categories %}
                <button class="btn btn-sm btn-primary btn-raised">{{ c_slug }}</button>
            {% else %}
                <a href="/category/{{ c_slug }}" class="btn btn-sm btn-default btn-raised">{{ c_slug }}</a>
            {% endif %}
        {% endfor %}
    {% endfor %}