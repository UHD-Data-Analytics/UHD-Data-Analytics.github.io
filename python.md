---
layout: default
title: "Python "Notes"
permalink: /python/
---
{% for document in site.python %}

<h2><a href = "{{document.url | prepend: site.baseurl }}">{{ document.title }}</a></h2>
<p>
{{ document.description }}
</p>

{% endfor %}
