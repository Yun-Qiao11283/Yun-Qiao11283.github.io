---
permalink: /research/
title: "Research"
author_profile: true
description: "Yun Qiao's research interests and selected projects in computational mathematics and topological data analysis."
---

My research interests lie in **large-scale computational optimization**, **numerical linear algebra**, and **topological data analysis**. I am interested in mathematical and computational methods for understanding complex, high-dimensional systems.

## Research projects

{% for project in site.data.research %}
### {{ project.title }}

**{{ project.dates }}** · {{ project.institution }}<br>
Supervised by **{{ project.supervisor }}**

{{ project.summary }}

[GitHub]({{ project.github }}){% if project.poster %} · [Project poster]({{ project.poster }}){% endif %}

{% unless forloop.last %}
---
{% endunless %}
{% endfor %}
