---
title: "Research"
permalink: /test3/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{{ site.categories-order[0] }}

{% for category in docs_by_category %}
  <div class="category_wrapper">
	{{ category["name"] }}
	{{ category["name"] | first }}
	{{ category["name"] | last }}
	{{ category["name"] | lstrip }}
	{{ category["name"] | rstrip }}
	{{ category["name"] | escape_once }}
    <ul>
    {% for item in category.items reversed %}

	{{ item.categories }}

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