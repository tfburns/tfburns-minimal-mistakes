---
title: "Test2"
permalink: /test2/
author_profile: true
comments: false
layout: single
date: 2024-08-11
---

<!-- {% assign entries_layout = page.entries_layout | default: 'list' %}
{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
  {% unless collection.output == false or collection.label == "posts" %}
    <section class="taxonomy__section">
      {% capture label %}{{ collection.label }}{% endcapture %}
      {% if label != written_label %}
        <h2 id="{{ label | slugify }}" class="archive__subtitle">{{ label }}</h2>
        {% capture written_label %}{{ label }}{% endcapture %}
      {% endif %}
      <div class="entries-{{ entries_layout }}">
        {% for post in collection.docs %}
          {% include archive-single.html type=entries_layout %}
        {% endfor %}
      </div>
      <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
    </section>
  {% endunless %}
{% endfor %} -->

{% assign docs_by_category = site.documentation | group_by: "category" %}
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