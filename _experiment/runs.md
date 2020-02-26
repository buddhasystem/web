---
title: Summary of Runs
layout: default
abbrev: runs
weight: 4
---

# Summary of Runs


<table width="80%">

<tr>
<th>run</th><th>period</th><th>coordinator</th>
</tr>

{% for run in site.data.runs %}
<tr>
<td>{{ run.run }}</td><td>{{ run.period }}</td><td>{{ run.coordinator }}</td>
</tr>
{% endfor %}

</table>
