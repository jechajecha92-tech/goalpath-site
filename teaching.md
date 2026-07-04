---
title: Teaching
description: >-
  Teaching philosophy, courses, and student supervision by Jecha S Jecha at
  Zanzibar University.
permalink: /teaching/
---
## Teaching philosophy

I teach in the Faculty of Science at Zanzibar University, where I have worked
with students since 2017. My teaching combines practical information
technology skills with the pedagogy needed to put them to use — a natural
extension of my own background in IT with education and my research on how
technology is adopted in higher education.

Three commitments run through my teaching:

- **Make the implicit explicit.** Digital and research skills are teachable;
  I build them into practical sessions rather than assuming students arrive
  with them.
- **Technology in context.** Educational technology is only useful when it
  works in the classroom students actually have. I favour tools that survive
  low bandwidth, shared devices, and power interruptions.
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

I welcome project ideas connected to information technology, educational
technology, or AI in education — students are encouraged to
[contact me](/contact/) with a one-paragraph proposal.
