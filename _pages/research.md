---
permalink: /research/
title: "Research"
author_profile: true
description: "Yun Qiao's research in computational mathematics and scientific computing, with current interests in large-scale optimization and numerical linear algebra."
---

I am broadly interested in **computational mathematics and scientific computing**, with current interests in **large-scale optimization and numerical linear algebra**. I am particularly interested in numerical algorithms that exploit mathematical structure to solve large-scale problems efficiently and reliably.

Topics that currently interest me include second-order and quasi-Newton optimization methods, iterative methods for large linear systems, preconditioning, and Krylov subspace methods.

My previous research has also involved topological data analysis and computational methods for high-dimensional data.

## Research Projects

{% for project in site.data.research %}
### {{ project.title }}

**{{ project.dates }} · {{ project.institution }}**<br>
**Advisor:** {{ project.supervisor }}

{{ project.summary }}

{% if project.methods %}**Methods:** {{ project.methods }}{% endif %}

[GitHub Repository]({{ project.github }}){% if project.poster %} · [Project Poster]({{ project.poster }}){% endif %}

{% unless forloop.last %}
---
{% endunless %}
{% endfor %}
