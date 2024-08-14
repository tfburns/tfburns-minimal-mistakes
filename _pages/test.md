---
title: "Test"
permalink: /test/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% for paper in site.research reversed %}
  
  <h3><a href="{{ paper.url }}">{{ paper.title }}</a><h2>
  <h6><i>{{ paper.excerpt }}</i></h6>
{% endfor %}