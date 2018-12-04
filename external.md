---
layout: default
title: "External Links"
---

<p>
    The following links lead to external resources to learn more about the data analytics programming languages and popular libraries.
</p>

<h2>Python Links</h2>
{% for nav in site.data.python %}
<h5><a href="{{ nav.url }}">{{ nav.text }}</a></h5>
{% endfor %}
</br></br>
<h2>R Links</h2>
{% for nav in site.data.r %}
<h5><a href="{{ nav.url }}">{{ nav.text }}</a></h5>
{% endfor %}
</br></br>
