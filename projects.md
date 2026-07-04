---
title: Projects
subtitle: Research software and academic projects.
description: >-
  Research software and academic projects by Jecha S Jecha, including
  learning analytics tools and AI-supported learning interventions.
permalink: /projects/
---
<div class="card-grid" markdown="0">
{% for project in site.data.projects %}
{% include project-card.html project=project heading="h2" %}
{% endfor %}
</div>
