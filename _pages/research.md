---
permalink: /research/
title: "Research"
author_profile: true
description: "Yun Qiao's research in computational mathematics and scientific computing, with current interests in large-scale optimization and numerical linear algebra."
---

I am broadly interested in **computational mathematics and scientific computing**, with current interests in **large-scale optimization and numerical linear algebra**. I am particularly interested in numerical algorithms that exploit mathematical structure to solve large-scale problems efficiently and reliably.

Topics that currently interest me include second-order and quasi-Newton methods, randomized sketching, preconditioning, Krylov subspace methods, and efficient sparse linear algebra, with applications to PDE-constrained optimization and high-dimensional machine learning.

My research experience also includes human-preference benchmarking for LLM responses and topological data analysis of financial time series.

## Research Projects

{% for project in site.data.research %}
### {{ project.title }}

**{{ project.dates }} · {{ project.institution }}**<br>
{% if project.role %}{{ project.role }}<br>{% endif %}
**{{ project.advisor_label | default: "Advisor" }}:** {{ project.supervisor }}

{{ project.summary }}

{% if project.methods %}**Methods:** {{ project.methods }}{% endif %}

{% if project.github %}[GitHub Repository]({{ project.github }}){% endif %}{% if project.poster %}{% if project.github %} · {% endif %}[Project Poster]({{ project.poster }}){% endif %}

{% unless forloop.last %}
---
{% endunless %}
{% endfor %}

## Research Manuscript

**LLMAdBench: A Human Preference Benchmark for Advertising in LLM Responses.**<br>
Co-author. **Manuscript under review at ICLR 2027.**
