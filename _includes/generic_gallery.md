# {{ page.title }}
{% assign type=include.type %}
{% assign run=include.run %}
{% assign images = site.data.gallery | where: "type", type | where: "gallery", true | sort: 'weight' %}

{% if run and run!='' %}
{% assign images = images | where: "run", run %}
{% endif %}

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
