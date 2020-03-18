---
title: Documents
abbrev: documents
layout: default
level: 0
weight: 10
document_folder: '/assets/documents/'
---

{% assign overviews = site.data.documents | where: "category", "overview" %}
{% assign summaries = site.data.documents | where: "category", "summary" %}
{% assign detectors = site.data.documents | where: "category", "detector" %}
{% assign systems   = site.data.documents | where: "category", "systems" %}
{% assign dra       = site.data.documents | where: "category", "dra" %}

# Documents

## General Overviews
<ul>
{% for item in overviews %}
<li><a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a></li>
{% endfor %}
</ul>

## Detector Subsystems
<ul>
{% for item in detectors %}
<li><a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a></li>
{% endfor %}
</ul>

## PHENIX Systems
<ul>
{% for item in systems %}
<li><a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a></li>
{% endfor %}
</ul>

## Summaries
<ul>
{% for item in summaries %}
<li><a href="{{ page.document_folder | append: item.name | relative_url }}" target="_blank">{{ item.title }}</a></li>
{% endfor %}
</ul>
