{% assign lumi_title = page.title | append: " Luminosity accumulation and related data" %}
{% include generic_gallery.md type="lumi" run=page.abbrev title=lumi_title columns=3 %}
{% include generic_gallery.md type="lumi" run=page.abbrev title=" " columns=1 gallery="aux" %}
