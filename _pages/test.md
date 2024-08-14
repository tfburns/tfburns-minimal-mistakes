---
title: "Test"
permalink: /test/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% for paper in site.research %}
  <h3><a href="{{ paper.url }}">{{ paper.title }}</a><h3>
{% endfor %}