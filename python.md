---
layout: default
title: "Python "Notes"
---
{% for document in site.python %}

<a href = "{{document.url | prepend: site.baseurl }}">
	<h2>{{ document.title }}</h2>
<p>
{{ document.description }}
</p>

{% endfor %}