---
title: Muon Tracker
role: Measures the position and momentum of muon particles.
abbrev: muon_tracker
layout: detector_base
image: '/images/detectors/phenix_quartercut_mutr.png'
image_title: 'PHENIX Quarter Cut with the Muon Tracker highlighted'
weight: 0
level: 1
category: muon
---
# {{ page.title }}

{% assign detector = page.abbrev %}
{% assign image = page.image %}
{% assign image_title = page.image_title %}

{% include include_image.md detector=detector image=image image_title=image_title %}
