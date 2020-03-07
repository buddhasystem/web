
{% assign title=page.title %}
{% assign alt_title=include.title %}

{% if alt_title and alt_title!='' %}
{% assign title = alt_title %}
{% endif %}

{% assign type=include.type %}
{% assign run=include.run %}
{% assign images = site.data.gallery | where: "type", type | where: "gallery", true | sort: 'weight' %}

{% if run and run!='' %}
{% assign images = images | where: "run", run %}
{% endif %}

{% assign length = images | size %}

{% if length!=0 %}
# {{ title }}
<table width="100%">

{% tablerow image in images cols:2 %}

{% if image.title !='' %}
<b>{{ image.title }}</b><br/>
{% endif %}

<a href="{{ image.path | relative_url }}">
<img src="{{ image.path | relative_url }}" alt="{{ image.title}}" height="300px"/>&nbsp;<br/><p/>
</a>
{% endtablerow %}

</table>

{% endif %}
