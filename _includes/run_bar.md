<table width="100%">

{% tablerow run in site.runs cols:16 %}
<a href="{{ run.url | relative_url }}">{{ run.title }}</a>
{% endtablerow %}

</table>
