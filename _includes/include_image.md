{% if include.image!='' %}
<h4>{{ include.image_title }}</h4>
<a href="{{ include.image | relative_url }}">
<img src="{{ include.image | relative_url }}" alt="?" width="{{ layout.image_width }}px"/>
</a>
{% endif %}

