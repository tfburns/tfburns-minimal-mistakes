---
title: "Test4"
permalink: /test4/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

<!-- {% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% for category in site.categories-order %}
  {{category.name}}
{% endfor %} -->

{% assign groups = site.research | group_by: "categories" | sort: "name" %}

{% for group in groups %}
    {{ group.name }}
    {% for item in group.items reversed %}
		<li class="collapsed">
          <a href="{{ site.baseurl }}{{ item.url }}">
          {% if item.url == navurl %}
            <u>{{ item.title }}</u>
          {% else %}
            {{ item.title }}
          {% endif %}
          </a>
      </li>
    {%endfor%}
{%endfor%}