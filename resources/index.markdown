---
layout: default
title: Learning resources
---

<div class="container-fluid cover-joinus">
	<div class="row">
		<div class="col-md-12">
			<div class="page-dscr">
				<p>Are you a Code Kitten, who wants to dip her paws into the world of coding? We've collected our favorite resources from around the web that can help you make the first steps.</p>
				{% assign all_resources = site.data.resources | order_by: "order" %}
				{% for category_hash in all_resources reversed %}
				{% assign category = category_hash[1] %}
				<h2>{{ category.category }}</h2>
				<div class="break"></div>
				<p>{{ category.description }}</p>
				<ul>{% assign category_links = category.links | sort: "date" %}
					{% for link in category_links reversed %}
						<li>
							<a href="{{ link.url }}" target="_blank">{{ link.title }}</a>
							{% if link.about %} - {{ link.about }}{% endif %}
						</li>
					{% endfor %}
				</ul>
				{% endfor %}

			</div>
		</div>
		<div class="col-md-8">
			<img class="illu-about" src="/assets/images/illustrations/catz_back_fill.png" >
		</div>
	</div>
</div>