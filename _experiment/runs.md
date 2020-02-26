---
title: Summary of Runs
layout: default
abbrev: runs
weight: 4
---

# Summary of Runs


<table width="100%">

<tr>
<th>Run</th><th>Period</th><th>Coordinator</th>
</tr>

{% for run in site.data.runs %}
<tr>
<td>{{ run.run }}</td><td>{{ run.period }}</td><td>{{ run.coordinator }}</td>
</tr>
{% endfor %}

</table>
