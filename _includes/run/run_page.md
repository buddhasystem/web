{% include run/run_bar.md %}
<hr/>
<center><h2>{{ page.title }}</h2></center>
<hr/>

{% assign images = site.data.gallery | where: "type", "run_configuration" | where: "run", page.run %}
{% assign length = images | size %}

{% if length!=0 %}
{% assign image=images[0].path %}
{% assign title=images[0].title %}
{% assign width=images[0].width %}


<table width="100%">
<tr><th>Configuration Diagram</th><th>RHIC run record</th></tr>

<tr>

<td>
{% if image!='' %}
{% include include_image.md image=image title='' width=width %}
{% else %}
&nbsp;
{% endif %}
</td>

<td>
{% include rhic_record.md run=page.run %}
</td>

</tr>

</table>

{% endif %}

{% include lumi_page.md %}
