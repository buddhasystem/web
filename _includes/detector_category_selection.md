# {{ page.title }}

<table WIDTH="100%">

<tr>
<th>Name</th><th>Role</th>
</tr>
{% assign items = site.detectors | sort: 'weight' %}

{% for detector in items %}

{% if detector.category == page.detector_category %}
{% include detector_category.md content=detector %}
{% endif %}

{% endfor %}

</table>
