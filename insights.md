---
title: AI Insights
subtitle: Notes on artificial intelligence, its adoption, and how students actually learn.
description: >-
  AI Insights — the academic blog of Jecha S Jecha on AI in education, AI
  adoption in higher education, and self-regulated learning.
permalink: /insights/
---
<div markdown="0">
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    {% include post-card.html post=post heading="h2" %}
  </li>
  {% endfor %}
</ul>
<p><a href="{{ '/feed.xml' | relative_url }}">Subscribe via RSS</a></p>
</div>
