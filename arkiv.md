---
layout: archive
title: Arkivet
permalink: /arkiv/
---

{% for post in site.posts %}
  <span class="left gray margin">{{ post.date | date: "%d.%m.%Y" }}</span>
  <span class="left">[{{ post.title }}]({{ post.url }})</span>

<p class="clear"></p>

{% endfor %}