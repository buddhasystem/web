---
title: Documents
abbrev: documents
layout: default
level: 0
weight: 10
document_folder: '/assets/documents/'
---
# Documents

<ul>
{% for item in site.data.documents %}
<li>
<a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a>
</li>
{% endfor %}
</ul>



<li>
<a href="{{ '/assets/documents/PHENIXSpin.pdf' | relative_url }}" target="_blank">PHENIX Spin Program Summary Table</a>
</li>
