---
title: Publications
subtitle: Journal papers, conference papers, book chapters, working papers, and preprints.
description: >-
  Publications by Jecha S Jecha on AI in education, academic
  procrastination, self-regulated learning, and learning analytics — with
  abstracts, DOIs, and BibTeX.
permalink: /publications/
---
<div markdown="0">
{% assign groups = "journal|Journal papers,conference|Conference papers,chapter|Book chapters,working|Working papers,preprint|Preprints" | split: "," %}
{% for group in groups %}
{% assign parts = group | split: "|" %}
{% assign type_key = parts[0] %}
{% assign type_label = parts[1] %}
{% assign pubs = site.data.publications | where: "type", type_key %}
{% if pubs.size > 0 %}
<section aria-labelledby="pubs-{{ type_key }}">
  <h2 id="pubs-{{ type_key }}">{{ type_label }}</h2>
  {% for pub in pubs %}
  {% include publication.html pub=pub id_prefix="pubs" %}
  {% endfor %}
</section>
{% endif %}
{% endfor %}
</div>
