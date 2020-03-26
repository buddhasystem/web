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

<tr>
{% if include.run %}
{% else %}
<th style="text-align:center">Run</th>
{% endif %}
<th style="text-align:center">Species</th>
<th style="text-align:center">Energy<br/>(GeV/nucleon)</th>
<th style="text-align:center">Integrated<br/>Luminosity<br/>[Polarization L/T]</th>
<th style="text-align:center">N<sub>events</sub><br/>[BBC<sub>30cm</sub>/BBC<sub>narrow</sub>]</th>
</tr>


{% for run in run_list %}

{% if run.rhic %}
{% assign runno=run.run | replace: "run", "" %}

{% for period in run.rhic %}
<tr>
{% if include.run %}
{% else %}
{% assign run_link = '/runs/' | append: run.run | append: '.html' | relative_url %}
<td style="text-align:center"><a href="{{ run_link }}"> {{ runno }}</a></td>
{% endif %}
<td style="text-align:center">{{ period['species'] }}</td>
<td style="text-align:center">{{ period['energy'] }}</td>
<td style="text-align:center">{{ period['lumi'] }}</td>
<td style="text-align:center">{{ period['Nevents'] }}</td>
</tr>

{% assign runno=' ' %}
{% endfor %}


{% endif %}

{% endfor %}
</table>

{% else %}

Data to be added soon, work in progress.

{% endif %}
