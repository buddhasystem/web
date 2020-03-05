---
title: Contact us
layout: default
abbrev: contact
weight: 1
---

# Contact us

These pages are designed and maintained by the PHENIX Data and Analysis Preservation task force members:

<table width="40%">
{% for who in site.data.people %}
<tr>
<td>{{ who.full }}</td><td><a href="mailto:{{ who.email }}">{{ who.email }}</a></td>
</tr>
{% endfor %}
</table>
