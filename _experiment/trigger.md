---
title: Trigger Information
layout: newbase
abbrev: trigger
level: 0
weight: 30
document_folder: '/assets/documents/'
---

{% include title.md %}


### EMCal/RICH trigger (ERT)
The EMCal/RICH trigger (ERT) selects events with high-p<sub>T</sub> electromagnetic probes or
the presence of heavy flavor decays.

<b>References</b>
{% assign items = site.data.documents %}
<ul>
{% for item in items %}
{% if item.tags contains 'ert' %}
<li><a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a></li>
{% endif %}
{% endfor %}
</ul>