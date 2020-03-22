---
title: Muon Arm Detectors
abbrev: muon_arm
layout: default
weight: 30
level: 0
detector_category: "muon"
---
{% include detectors/detector_category_selection.md %}

# Development area

{% assign detectors = site.data.detectors | where: "category", "muon" %}
{% assign pages = site.detectors | sort: 'weight' %}

{% for detector in detectors %}
{% assign selected_pages = pages | where: "abbrev", detector.abbrev %}
{% assign page=selected_pages[0] %}
{% include detectors/detector_link.md page=page detector=detector %}
{% endfor %}
