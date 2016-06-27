---
layout: archive
title: Posts
tags: []
modified: 
comments: false
author_profile: true
---

<div id="main" role="main">
  <div id="index">
    {% capture written_year %}'None'{% endcapture %}
    {% for post in site.posts %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% if year != written_year %}
        <h3>{{ year }}</h3>
        {% capture written_year %}{{ year }}{% endcapture %}
      {% endif %}
      <article>
        {% if post.link %}
          <h2 class="link-post"><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> <a href="{{ post.link }}" target="_blank" title="{{ post.title }}"><i class="fa fa-link"></i></a></h2>
        {% else %}
          <h2><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h2>
          <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
        {% endif %}
      </article>
    {% endfor %}
  </div><!-- /#index -->
</div><!-- /#main -->
