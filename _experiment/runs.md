---
title: Summary of Runs
layout: default
abbrev: runs
weight: 3
---

# Summary of Runs


<table width="100%">

<tr>
<th>Run</th><th>Period</th><th>Coordinator(s)</th>
</tr>

{% for run in site.runs %}
<tr>
<td>{{ run.title }}</td><td>{{ run.period }}</td><td>{{ run.coordinator }}</td>
</tr>
{% endfor %}

</table>
