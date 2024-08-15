---
title: "Test2"
permalink: /test2/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% for my_doc in site.research %}

{% for category in my_doc.categories %}
  {% capture my_categories %}
    {% if my_categories %}
      {{ my_categories | join: "," }},{{ category }}
    {% else %}
       {{ category }}
    {% endif %}
  {% endcapture %}
{% endfor %}

{% endfor %}

{% assign my_categories = my_categories | split: "," | uniq %}

{% for cat in my_categories %}
  {{cat }}
{% endfor %}