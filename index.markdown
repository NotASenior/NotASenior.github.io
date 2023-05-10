---
layout: default
title: Not a Senior's Blog
---

<!-- # C# from zero to something 

Disclaimer: este blog aun está siendo construido. Faltan muchas cosas por configurar, así que no esperes un artículo semanal aún. Puede que pase, puede que no -->

<!-- <ul>
    {% for post in site.categories['tutorial'] reversed %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul> -->

# Artículos

Disclaimer: este blog aun está siendo construido. Faltan muchas cosas por configurar, así que no esperes un artículo semanal aún. Puede que pase, puede que no

<ul>
    {% for post in site.posts reversed %}
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>