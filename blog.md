---
layout: page
title: About
permalink: blog.html
---

{% for post in site.posts  %}
    {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

    {% if forloop.first %}
<h3 id="{{ this_year }}-ref">{{this_year}}</h3>
<ul>
    {% endif %}
	<li>
	<p class="blogentry">
	<a href="{{ post.url }}">{{ post.title }}</a>
	</p>
	<p class="blogdesc">
	Posted {{ post.date | date_to_string }} in
	{% for category in post.categories %}
		{% unless forloop.last %}
			{{ category }},
		{%else %}
			{{ category }}
		{% endunless %}
	{% endfor %}
	</p>
	</li>
    {% if forloop.last %}
</ul>
    {% else %}
        {% if this_year != next_year %}
</ul>
<h3 id="{{ next_year }}-ref">{{next_year}}</h3>
<ul>
        {% endif %}
    {% endif %}
{% endfor %}