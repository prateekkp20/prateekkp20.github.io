---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% assign sections = "Manuscripts under review|Conference proceedings|Presentations" | split: "|" %}
{% assign items = site.publications | sort: "date" | reverse %}

{% for section in sections %}
  <h2 class="archive__subtitle">{{ section }}</h2>
  {% for post in items %}
    {% if post.type == section %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}
{% endfor %}
