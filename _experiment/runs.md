---
title: Summary of Runs
layout: default
abbrev: runs
level: 0
weight: 20
---

# Summary of Runs


<table width="100%">

<tr>
<th>Run</th><th>Period</th><th>Coordinator(s)</th>
</tr>

{% for run in site.runs %}

{% include run_short.md run=run %}

{% endfor %}

</table>
<hr/>
{% include generic_gallery.md type="run_info" gallery="aux" title="Summary tables (click for larger image)" %}
