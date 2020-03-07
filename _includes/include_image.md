{% if include.image!='' %}

{% assign width=layout.image_width %}
{% if include.width %}
{% assign width=include.width %}
{% endif %}


<h3>{{ include.title }}</h3>
<a href="{{ include.image | relative_url }}">
<img src="{{ include.image | relative_url }}" alt="?" width="{{ width }}px"/>
</a>
{% endif %}

