---
layout: archive
title: Arkivet
permalink: /arkiv/
---

{% if post in site.posts %}
	{% for post in site.posts %}
  		<span class="left gray margin">{{ post.date | date: "%d.%m.%Y" }}</span>
  		<span class="left">[{{ post.title }}]({{ post.url }})</span>

<p class="clear"></p>

	{% endfor %}
{% else %}
    <p>Det er ingen artikler i arkivet.</p>
{% endif %}