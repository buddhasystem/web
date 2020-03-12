---
title: Summary of Runs
layout: default
abbrev: runs
level: 0
weight: 20
---

## Summary of Runs


<table width="100%">

<tr>
<th>Run</th><th>Period</th><th>Coordinator(s)</th>
</tr>

{% for run in site.runs %}

{% include run_short.md run=run %}

{% endfor %}

</table>
<hr/>
{% include generic_gallery.md type="run_info" gallery="aux" title="PHENIX run summary tables (click for larger image)" %}
<hr/>

## RHIC Run Records
<table width="100%">
<tr>
<th>Run</th><th>Species</th><th>Energy (GeV/nucleon)</th>
</tr>

{% for run in site.data.runs %}
{% if run.rhic %}
{% assign runno=run.run %}

{% for period in run.rhic %}
<tr>
<td>{{ runno }}</td>
<td>{{ period['species'] }}</td>
<td>{{ period['energy'] }}</td>
</tr>
{% assign runno=' ' %}
{% endfor %}

{% endif %}

{% endfor %}
</table>
