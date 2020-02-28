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
{% include detector_category.md content=detector %}
{% endif %}

{% endfor %}

</table>
