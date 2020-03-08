{% include run_bar.md %}
<hr/>
<center><h2>{{ page.title }}</h2></center>
<hr/>

{% assign images = site.data.gallery | where: "type", "run_configuration" | where: "run", page.abbrev | sort: 'weight' %}
{% assign length = images | size %}

{% if length!=0 %}
{% assign image=images[0].path %}
{% assign title=images[0].title %}
{% assign width=images[0].width %}

{% assign detector = page.abbrev %}

{% if image!='' %}
{% include include_image.md detector=detector image=image title=title width=width %}
{% endif %}

{% endif %}

{% include lumi_page.md %}
