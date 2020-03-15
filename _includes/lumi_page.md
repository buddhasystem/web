{% assign lumi_title = page.title | append: " Luminosity accumulation and related data" %}

{% include images/generic_gallery.md type="lumi" run=page.run title=lumi_title columns=3 %}
{% include images/generic_gallery.md type="lumi" run=page.run title=" " columns=1 gallery="aux" %}
