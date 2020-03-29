{% if include.title %}
## {{ include.title }}
{% endif %}

{% assign items = site.data.documents | where: "category", include.category %}

<ul>
{% for item in items %}
<li><a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a></li>
{% endfor %}
</ul>

