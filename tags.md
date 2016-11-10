---
layout: archive
title: Tags
modified: 
comments: false
author_profile: true
---

<div id="main" role="main">
  <div id="index">
    {% capture tags %}
      {% for tag in site.tags %}
        {{ tag[0] }}
      {% endfor %}
    {% endcapture %}
    {% assign sortedtags = tags | split:' ' | sort %}

    {% for tag in sortedtags %}
      <h3 id="{{ tag }}">{{ tag }}</h3>
      <ul>
      {% for post in site.tags[tag] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
      </ul>
    {% endfor %}
  </div><!-- /#index -->
</div><!-- /#main -->
