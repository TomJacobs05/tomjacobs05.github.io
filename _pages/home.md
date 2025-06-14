---
title: "Home"
layout: homelay
sitemap: false
permalink: /
---

I am a PhD candidate at [CISPA Helmholtz Center for Information Security](https://cispa.de) in Saarbrücken, Germany. 

My research interests lie at the intersection of understanding neural network training dynamics and designing efficient deep learning methods. Concretely, I work with theoretical tools from non-convex optimization and mathematical analysis such as mirror flow, explicit regularization, mean field descriptions and stochastic differential equations to study the effect of overparameterization, improve model efficiency, and improve generalization performance.



{% if site.data.news %}
<br>
<div class="well" style="padding: 0px">
#### Updates
  <div style="display: block; padding: 10px">
<!-- how many future events to render -->
{% assign render_limit = 5 %}
<!-- counter of rendered events -->
{% assign rendered = 0 %}
<!-- iterate over events -->
{% for event in site.data.news %}
<!-- check if limit was reached -->
{% if rendered == render_limit %}
{% break %}
{% endif %}
* <strong>{{ event.date | date: "%-d.%m.%y" }} ⋙</strong> {{ event.description }}
<!-- increase counter of rendered events -->
{% assign rendered = rendered | plus:1 %}
{% if forloop.last == false %}
<!-- <hr style="margin: 10px -10px;"> -->
{% endif %}
{% endfor %}
</div>
</div>
{% endif %}

