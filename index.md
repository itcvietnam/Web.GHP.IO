---
layout: default
title: Index
description: Description for index
---
<p>Index (2)</p>

{% assign docs = site.categories.docs | where:"status","yes" %}
{% assign expDocs = site.categories.docs | where_exp:"item","item.status == yes" %}
<ol style="color: green;">
    {% for post in docs %}
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

<h2>Docs:</h2>
<ul>
    {% for doc in site.docs %}
        <li><a href="{{ site.url }}/Web.GHP.IO{{ doc.url }}">{{ doc.title }}</a></li>
    {% endfor %}
</ul>

<hr />

<ul>
    {% for post in site.data.blogs %}
        <li>{{ post.title }}</li>
    {% endfor %}
</ul>

<p>{{ site.data.info.copyright }}</p>