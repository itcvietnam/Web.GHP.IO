---
layout: default
title: Index
description: Description for index
---
<p>Index (2)</p>

<ul>
    {% for category in site.categories %}
        <li><a href="{{ site.url }}/category/{{ category | first | slugify }}/index.html">{{ category | first }}</a></li>
    {% endfor %}
</ul>