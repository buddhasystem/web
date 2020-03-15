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

{% include run/run_short.md run=run %}

{% endfor %}

</table>
<hr/>
{% include images/generic_gallery.md type="run_info" gallery="aux" title="PHENIX run summary tables (click for larger image)" %}
<hr/>

{% include rhic/rhic_record.md title="RHIC run records" %}