---
title: Central Arm
abbrev: central_arm
layout: default
weight: 3
level: 0
---
# Central Arm Detectors

<table WIDTH="100%">

<tr>
<th>Name</th><th>Role</th>
</tr>

{% for detector in site.detectors %}

{% if detector.category == "central" %}
<tr>
<td><a href="{{ detector.url | relative_url }}">{{ detector.name }}</a></td><td>{{ detector.role }}</td>
</tr>
{% endif %}

{% endfor %}

</table>
