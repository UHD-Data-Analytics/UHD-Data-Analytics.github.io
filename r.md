---
layout: default
title: "R "Notes"
---
{% for document in site.r %}

<h2><a href = "{{document.url | prepend: site.baseurl }}">{{ document.title }}</a></h2>
<p>
{{ document.description }}
</p>

{% endfor %}
