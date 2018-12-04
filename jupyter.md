---
layout: default
title: "Jupyter "Notes"
---
{% for document in site.jupyter %}

<h2><a href = "{{document.url | prepend: site.baseurl }}">{{ document.title }}</a></h2>
<p>
{{ document.description }}
</p>

{% endfor %}
