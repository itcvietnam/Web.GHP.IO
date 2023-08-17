---
layout: default
title: Index
description: Description for index
---
<link href="{{ site.url }}/Web.GHP.IO/assets/css/style.css" rel="stylesheet">

<p>Index (1)</p>

<ol>
    {% for post in site.categories.docs %}
        <li><a href="{{ site.url }}/Web.GHP.IO{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ol>
<ol>
    {% for post in site.categories.blog %}
        <li><a href="{{ site.url }}/Web.GHP.IO{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ol>
<ol>
    {% for post in site.categories[site.data.category.blog] %}
        <li><a href="{{ site.url }}/Web.GHP.IO{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ol>

<ul>
    {% for category in site.categories %}
        <li>
            <h4>{{ category[0] }}</h4>
            <ul>
                {% for post in category[1] %}
                    <li><a href="{{ site.url }}/Web.GHP.IO{{ post.url }}">{{ post.title }}</a></li>
                {% endfor %}
            </ul>
        </li>
    {% endfor %}
</ul>

<hr />

<ul>
    {% for post in site.data.blogs %}
        <li>{{ post.title }}</li>
    {% endfor %}
</ul>

<p>{{ site.data.info.copyright }}</p>

<script src="{{ site.url }}/Web.GHP.IO/assets/js/script.js"></script>