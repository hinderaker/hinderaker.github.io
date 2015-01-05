---
layout: archive
title: Arkivet
permalink: /arkiv/
---

{% if post in site.posts %}
    {% for post in site.posts %}
        {% capture post_year %}{{ post.date | date: '%Y' }}{% endcapture %}
        {% if forloop.first %}
            <h3>{{ post_year }}</h3>
        {% endif %}
		
        {% if forloop.first == false %}
            {% assign previous_index = forloop.index0 | minus: 1 %}
            {% capture previous_post_year %}{{ site.posts[previous_index].date | date: '%Y' }}{% endcapture %}
            {% if post_year != previous_post_year %}
                <h3>{{ post_year }}</h3>
            {% endif %}
        {% endif %}
		
        <span class="left gray margin">{{ post.date | date: "%d.%m.%Y" }}</span>
        <span class="left"><a href="{{ post.url }}">{{ post.title }}</a></span>

        <p class="clear"></p>

        {% if forloop.last %}
        {% endif %}
    {% endfor %}
{% else %}
    <p>Det er ingen artikler i arkivet.</p>
{% endif %}