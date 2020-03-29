---
title: How to Contribute
layout: newbase
abbrev: howto
weight: 10
level: 0
---
{% assign find_site_page=site.about | where: "abbrev", 'site' %}
{% assign site_page_url=find_site_page[0].url  | relative_url %}

{% assign find_contacts_page=site.about | where: "abbrev", 'contact' %}
{% assign contacts_page_url=find_contacts_page[0].url  | relative_url %}

{% include title.md %}

### Welcome
Contributions from the PHENIX community are crucial for this project to succeed.
You are most welcome to get involved. Materials that you consider to be relevant
to the mission of the site can be sent for consideration to the members of the
<a href="{{ contacts_page_url }}">Data and Analysis Preservation task force</a>.

### Direct Contributions
If you are willing to contribute directly by developing the actual content
this will be even more valuable and greatly appreciated. For this, you will
need to have basic knowledge of the Web platform used on this <a href="{{ site_page_url }}">site</a>.
This assumes that you are familiar with basic features of *git*,
<a href="https://www.github.com/">GitHub</a>, and the
<a href="https://www.markdownguide.org/basic-syntax/">Markdown Syntax</a> (which is
really not hard at all). For optimal productivity, you should install the
<a href="http://jekyllrb.com/">Jekyll</a> web site generator on your laptop or workstation
which will allow you to test drive the updated site before you make commits to the repository.

### Advanced
The more adventerous and/or expert users can leverage
the following components of the platform:
* The <a href="https://shopify.github.io/liquid/">Liquid</a> template language
* The <a href="http://getbootstrap.com/">Bootstrap</a> toolkit.

