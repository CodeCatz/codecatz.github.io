---
layout: page
title: Learning resources
---

Are you a Code Kitten, who wants to dip her paws into the world of coding? We've collected our favorite resources from around the web that can help you make the first steps.

{% assign all_resources = site.data.resources | order_by: "order" %}
{% for category_hash in all_resources reversed %}
{% assign category = category_hash[1] %}

### {{ category.category }}

<div class="break"></div>

{{ category.description }}

{% assign category_links = category.links | sort: "date" %}
	{% for link in category_links reversed %}
- <a href="{{ link.url }}" target="_blank">{{ link.title }}</a>
			{% if link.about %} - {{ link.about }}{% endif %}
	{% endfor %}
{% endfor %}

<div class="col-md-8">
	<img class="illu-about" src="/assets/images/illustrations/catz_back_fill.png" >
</div>
