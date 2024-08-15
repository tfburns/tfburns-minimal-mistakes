---
title: "Research"
permalink: /research/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% for category in docs_by_category %}
  <div class="category_wrapper">
    {% for item in category.items reversed %}
	{% if forloop.first %}
	{{ item.categories }}
	<ul>
	{% endif %}
      <li class="collapsed">
		  <img src="{{ site.baseurl }}{{ item.header.teaser }}">
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