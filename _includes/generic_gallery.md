# {{ page.title }}
{% assign type=include.type %}
{% assign images = site.data.gallery | where: "type", type | sort: 'weight' %}

<table border="1" width="100%">

{% tablerow image in images cols:2 %}

{% if image.title !='' %}
{{ image.title }}<br/>
{% endif %}

<a href="{{ image.path | relative_url }}">
<img src="{{ image.path | relative_url }}" alt="{{ image.title}}" width="400px"/>&nbsp;<br/><p/>
</a>

{% endtablerow %}

</table>
