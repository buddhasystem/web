---
title: Documents
abbrev: documents
layout: default
level: 0
weight: 10
document_folder: '/assets/documents/'
items:
   - {title: 'General Overviews',			category: 'overview'}
   - {title: 'Detector Subsystems',			category: 'detector'}
   - {title: 'Data Reconstruction and Analysis',	category: 'dra'}
   - {title: 'PHENIX Systems',				category: 'systems'}
   - {title: 'Summaries',				category: 'summary'}
---
# Documents

{% for item in page.items %}
{% include documents/doc.md title=item.title category=item.category %}
{% endfor %}
