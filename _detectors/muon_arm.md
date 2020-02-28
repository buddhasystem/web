---
title: Muon Arm
abbrev: muon_arm
layout: default
weight: 4
level: 0
---
# Muon Arm Detectors

<table WIDTH="100%">

<tr>
<th>Name</th><th>Role</th>
</tr>
{% assign items = site.detectors | sort: 'weight' %}

{% for detector in items %}

{% if detector.category == "muon" %}
<tr>
<td><a href="{{ detector.url | relative_url }}">{{ detector.name }}</a></td><td>{{ detector.role }}</td>
</tr>
{% endif %}

{% endfor %}

</table>
