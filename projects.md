---
title: Projects
subtitle: Applied research, consultancy, and academic projects.
description: >-
  Applied research and consultancy by Jecha S Jecha, including digital
  economy and digital health work in Zanzibar and higher-education
  curriculum development.
permalink: /projects/
---
<div class="card-grid" markdown="0">
{% for project in site.data.projects %}
{% include project-card.html project=project heading="h2" %}
{% endfor %}
</div>
