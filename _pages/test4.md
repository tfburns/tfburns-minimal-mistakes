---
title: "Test3"
permalink: /test3/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% for cat in site.categories-order %}
  {% assign currentCat = docs_by_category | where: 'name', cat | first %}
  <div class="category_wrapper">
    <div class="category">{{ currentCat.name }}</div>
    <ul>
    {% for item in currentCat.items %}
      <li class="collapsed">
          <a href="{{ site.baseurl }}{{ item.url }}">
          {% if item.url == navurl %}
            <u>{{ item.title }}</u>
          {% else %}
            {{ item.title }}
          {% endif %}
          </a>
      </li>
    {% endfor %}
    </ul>
  </div>
{% endfor %}