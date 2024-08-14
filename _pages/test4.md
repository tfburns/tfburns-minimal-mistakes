---
title: "Test4"
permalink: /test4/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% for cat in site.categories-order %}
  {{cat.name}}
{% endfor %}