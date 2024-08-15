---
layout: archive
title: "Research (grid view)"
permalink: /research-archive-grid/
entries_layout: grid
author_profile: true
---

{% assign docs_by_category = site.research | group_by: "categories" | reverse %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
{% capture written_label %}'None'{% endcapture %}

{% for category in docs_by_category %}
    <section class="taxonomy__section">
      {% capture label %}{{ category.name }}{% endcapture %}
      {% if label != written_label %}
        <h2 id="{{ label | slugify }}" class="archive__subtitle">{{ label }}</h2>
        {% capture written_label %}{{ label }}{% endcapture %}
      {% endif %}
      <div class="entries-{{ entries_layout }}">
        {% for post in category %}
          {% include archive-single.html type=entries_layout %}
        {% endfor %}
      </div>
      <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
    </section>
{% endfor %}
