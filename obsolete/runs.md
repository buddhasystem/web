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

{% for run in site.data.runs %}
<tr>
<td>{{ run.run }}</td><td>{{ run.period }}</td><td>{{ run.coordinator }}</td>
</tr>
{% endfor %}

</table>
