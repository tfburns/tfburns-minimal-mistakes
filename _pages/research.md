---
title: Research
layout: home
permalink: /research/
collection: research
entries_layout: grid
classes: wide
---

{% include base_path %}

<div class="grid__wrapper">
  {% for post in site.research %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>