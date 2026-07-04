---
title: Curriculum Vitae
description: >-
  Academic CV of Jecha S Jecha — education, appointments, publications,
  skills, and service. Downloadable as PDF.
permalink: /cv/
---
<p><a class="button button--primary" href="{{ '/assets/files/jecha-s-jecha-cv.pdf' | relative_url }}" download>Download CV (PDF)</a></p>

## Education

{% for item in site.data.cv.education %}
**{{ item.degree }}**, {{ item.institution }}, {{ item.location }}
({{ item.period }}).
{{ item.detail }}
{% endfor %}

## Academic appointments

{% for item in site.data.cv.appointments %}
**{{ item.title }}**, {{ item.institution }}, {{ item.location }}
({{ item.period }}).
{{ item.detail }}
{% endfor %}

## Research interests

{% for interest in site.author.research_interests %}
- {{ interest }}
{%- endfor %}

## Publications

{% for pub in site.data.publications -%}
- {{ pub.authors }} ({{ pub.year }}). {{ pub.title }}.
  {%- if pub.venue %} *{{ pub.venue }}*.{% endif %}
  {%- if pub.status %} {{ pub.status }}.{% endif %}
{% endfor %}

See the [publications page](/publications/) for abstracts, DOIs, and BibTeX.

## Teaching

{% for course in site.data.teaching.courses %}
- **{{ course.title }}** — {{ course.institution }} ({{ course.role }})
{%- endfor %}

## Skills

{% for skill in site.data.cv.skills %}
- **{{ skill.area }}:** {{ skill.items }}
{%- endfor %}

## Awards & recognition

{% for item in site.data.cv.awards %}
- **{{ item.year }}** — {{ item.text }}
{%- endfor %}

## Consultancy & service

{% for item in site.data.cv.service %}
- {{ item }}
{%- endfor %}

## Contact

- Email: [{{ site.author.email }}](mailto:{{ site.author.email }}) (institutional) · [{{ site.author.email_personal }}](mailto:{{ site.author.email_personal }})
- Phone (China): {{ site.author.phone_china }}
- Phone (Tanzania): {{ site.author.phone_tanzania }}
