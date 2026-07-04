---
title: Teaching
description: >-
  Teaching philosophy, courses, and student supervision by Jecha S Jecha at
  Zanzibar University.
permalink: /teaching/
---
## Teaching philosophy

I teach the way I research: with the conviction that **students are capable
of regulating their own learning when the environment makes regulation
possible**. My courses are structured around frequent low-stakes deadlines,
explicit planning activities, and feedback that names strategies rather than
just scores — the same principles my research investigates at scale with AI.

Three commitments run through my teaching:

- **Make the implicit explicit.** Study skills, time management, and
  academic writing are teachable; I build them into the syllabus instead of
  assuming students arrive with them.
- **Technology in context.** Educational technology is only useful when it
  works in the classroom students actually have. My courses use tools that
  survive low bandwidth, shared devices, and power interruptions.
- **Honest use of AI.** Students will use AI assistants whether or not the
  syllabus mentions them. I teach when AI use supports learning, when it
  substitutes for it, and how to tell the difference.

## Courses

<div class="card-list" markdown="0">
{% for course in site.data.teaching.courses %}
<article class="card">
  <h3 class="card__title">{{ course.code }} — {{ course.title }}</h3>
  <p class="card__meta">{{ course.level }} &middot; {{ course.institution }} &middot; {{ course.role }}</p>
  <p>{{ course.description }}</p>
</article>
{% endfor %}
</div>

## Supervision

{% for item in site.data.teaching.supervision -%}
**{{ item.level }}**, {{ item.institution }}. {{ item.topics }}
{% endfor %}

I welcome project ideas connected to educational technology, study behavior,
or AI in education — students are encouraged to [contact me](/contact/) with
a one-paragraph proposal.
