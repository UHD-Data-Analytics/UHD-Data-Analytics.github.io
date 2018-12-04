---
layout: default
title: "Julia "Notes"
---
{% for document in site.julia %}

<h2><a href = "{{document.url | prepend: site.baseurl }}">{{ document.title }}</a></h2>
<p>
{{ document.description }}
</p>

{% endfor %}
