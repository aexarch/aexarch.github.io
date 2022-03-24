---
layout: post
title: Research
description: A selection of research I have done.
permalink: /research/
nav: true
---

<div class="post">

  <ul class="post-list">
    {%- assign research = site.research | reverse -%} 
    {% for item in research %}

    {% assign year = post.date | date: "%Y" %}

    <li>
      <h3>
        {% if post.redirect == blank %}
          <a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        {% else %}
        <a class="post-title" href="{% if post.redirect contains '://' %}{{ post.redirect }}{% else %}{{ post.redirect | relative_url }}{% endif %}">{{ post.title }}</a>
        {% endif %}
      </h3>
      <p>{{ post.description }}</p>
      <p class="post-meta"> {{ post.date | date: '%B %-d, %Y' }}
      </p>
    </li>

    {% endfor %}
  </ul>
</div>
