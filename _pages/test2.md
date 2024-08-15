---
title: "test2"
permalink: /test2/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% for category in docs_by_category %}

    {% for item in category.items reversed %}
	{% if forloop.first %}
	{{ item.categories }}
	{% endif %}
	<div class="category_wrapper">
    <ul>
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