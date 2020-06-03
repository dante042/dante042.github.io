---
layout: archive
permalink: /research 
title: "Research"
author_profile: true
header: 
  imege: "/assets/bg2.png" 
---

{% include base\_path %} {% include group-by-array collection=site.posts field="tags" %}

{% for tag in group\_names %}
 {% assign posts = group\_items\[forloop.index0\] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
     {% include archive-single.html %} 
  {% endfor %} 
{% endfor %}
