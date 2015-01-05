---
layout: archive
title: Arkivet
permalink: /arkiv/
---
{% for post in site.posts %}

{% unless post.next %}
  <h3>{{ post.date | date: '%Y' }}</h3>
{% else %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
  {% if year != nyear %}
    <h3>{{ post.date | date: '%Y' }}</h3>
  {% endif %}
{% endunless %}

<span class="left gray margin">{{ post.date | date: "%d.%m.%Y" }}</span>
<span class="left">[{{ post.title }}]({{ post.url }})</span>

<p class="clear"></p>

{% endfor %}