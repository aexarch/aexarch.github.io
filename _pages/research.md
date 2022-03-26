---
layout: page
title: research
description: 
permalink: /research/
nav: true
---

My research has largely focused on stochastic control, reinforcement learning, optimization, ML applications in neuroscience, and some differential game theory. You can view my doctoral dissertation [here](https://smartech.gatech.edu/handle/1853/59263).

<div class="post">

  <ul class="post-list">
    {%- assign research = site.research | reverse -%} 
    {% for item in research %}

    <li>
      <h3>
        {% if item.redirect == blank %}
          <a class="post-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
        {% else %}
        <a class="post-title" href="{% if item.redirect contains '://' %}{{ item.redirect }}{% else %}{{ item.redirect | relative_url }}{% endif %}">{{ item.title }}</a>
        {% endif %}
      </h3>
      <p>{{ item.description }}</p>
      <p class="post-meta"> {{ item.date | date: '%B %-d, %Y' }}
      </p>
    </li>

    {% endfor %}
  </ul>
</div>
