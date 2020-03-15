{% if include.title %}
## {{ include.title }}
{% endif %}


{% if include.run %}
{% assign run_list=site.data.runs | where: "run", include.run %}
{% else %}
{% assign run_list=site.data.runs %}
{% endif %}

{% if run_list[0].rhic %}

<table width="100%" border="1">
<tr><td><hr/></td><td><hr/></td><td><hr/></td></tr>
<tr>
<th style="text-align:center">Run</th>
<th style="text-align:center">Species</th>
<th style="text-align:center">Energy (GeV/nucleon)</th>
</tr>

{% for run in run_list %}

{% if run.rhic %}
{% assign runno=run.run | replace: "run", "" %}

{% for period in run.rhic %}
<tr>
<td style="text-align:center">{{ runno }}</td>
<td style="text-align:center">{{ period['species'] }}</td>
<td style="text-align:center">{{ period['energy'] }}</td>
</tr>
{% assign runno=' ' %}
{% endfor %}
<tr><td><hr/></td><td><hr/></td><td><hr/></td></tr>
{% endif %}

{% endfor %}
</table>

{% else %}

Data to be added soon, work in progress.

{% endif %}
