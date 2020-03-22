<table WIDTH="100%">

<tr><th>Name</th><th>Role</th></tr>

{% assign detectors = site.data.detectors | where: "category", include.category %}
{% assign pages = site.detectors | sort: 'weight' %}

{% for detector in detectors %}
{% assign selected_pages = pages | where: "abbrev", detector.abbrev %}
{% assign page=selected_pages[0] %}
{% include detectors/detector_link.md page=page detector=detector %}
{% endfor %}

</table>
