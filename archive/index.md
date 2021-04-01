---
layout: post
title: Archives
skip_related: true
---

{% assign totalwords = 0 %}
{% for post in site.posts %}
  {% assign wordcount = post.content | number_of_words %}
  {% assign totalwords = totalwords | plus: wordcount %}
{% endfor %}

{{ site.posts.last.date | date: "%Y" }}年{{ site.posts.last.date | date: "%M" }}月以来,我已经写了{{ totalwords }} 字。

<div id="archive">
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
<h2>{{ currentdate }}</h2>
<ul>
    {% assign date = currentdate %}
  {% endif %}
  <li {% if post.favorite and post.layout != "writeup" %}class="favorite"{% endif %}>
    <a href="{{ post.url }}">{{ post.title }}{% if post.layout == "writeup" %} (Book Writeup){% endif %}</a>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}
</div>


