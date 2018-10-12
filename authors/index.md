---
layout: page
current: authors
title: Authors
navigation: true
logo: 'assets/images/ghost.png'
class: page-template
subclass: 'post page'
---

<p style="text-align: center; line-height: 3em;">
{% capture site_authors %}{% for author in site.authors %}{{ author | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign authors = site_authors | split:',' | sort %}
{% include authorcloud.html %}
</p>
