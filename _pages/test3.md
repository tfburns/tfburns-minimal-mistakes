---
title: "Research"
permalink: /test3/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% for category in docs_by_category %}
  <div class="category_wrapper">
	{{ category.name | remove: "s"}}
	{{ category.title | remove: "e"}}
	{{ category.label | remove: "a"}}
    <ul>
    {% for item in category.items reversed %}
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