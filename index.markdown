---
layout: default
title: Not a Senior's Blog
---

# C# from zero to something 

<ul>
    {% for post in site.categories['tutorial'] reversed %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>