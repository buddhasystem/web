## RHIC Run Records
<table width="100%" border="1">
<tr>
<th style="text-align:center">Run</th>
<th style="text-align:center">Species</th>
<th style="text-align:center">Energy (GeV/nucleon)</th>
</tr>

{% for run in site.data.runs %}
{% if run.rhic %}
{% assign runno=run.run %}

{% for period in run.rhic %}
<tr>
<td style="text-align:center">{{ runno }}</td>
<td style="text-align:center">{{ period['species'] }}</td>
<td style="text-align:center">{{ period['energy'] }}</td>
</tr>
{% assign runno=' ' %}
{% endfor %}

{% endif %}

{% endfor %}
