{% include run_bar.md %}
<hr/>
# {{ page.title }}
{% assign images = site.data.gallery | where: "type", "run_configuration" | where: "run", page.abbrev | sort: 'weight' %}
{% assign length = images | size %}

{% if length!=0 %}
{% assign image=images[0].path %}
{% assign title=images[0].title %}

{% assign detector = page.abbrev %}

{% if image!='' %}
{% include include_image.md detector=detector image=image title=title %}
{% endif %}

{% endif %}