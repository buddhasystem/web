---
title: Contact us
layout: newbase
abbrev: contact
weight: 20
level: 0
div: yes
---

<h2> {{ page.title }} </h2>

These pages are designed and maintained by the PHENIX Data and Analysis Preservation task force members:<br/>
<p/>

<table width="80%">
{% for who in site.data.people %}
<tr>
<td>{{ who.full }}</td>
<td><a href="mailto:{{ who.email }}">{{ who.email }}</a></td>
<td>{{ who.role }}</td>
</tr>
{% endfor %}
</table>

