---
layout: default
title: "R Studio "Notes"
---
{% for document in site.rstudio %}

<h2><a href = "{{document.url | prepend: site.baseurl }}">{{ document.title }}</a></h2>
<p>
{{ document.description }}
</p>

{% endfor %}
