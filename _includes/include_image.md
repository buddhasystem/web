{% if include.image!='' %}

<h2>{{ include.title }}</h2>
<a href="{{ include.image | relative_url }}">
<img src="{{ include.image | relative_url }}" alt="?" width="{{ layout.image_width }}px"/>
</a>
{% endif %}

