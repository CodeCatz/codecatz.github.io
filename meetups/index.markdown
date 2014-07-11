---
layout: default
title: Our meetups recaps!
---


{% for post in site.posts %}
<div class="container-fluid">
	<div class="meetup">
		<h3><a href="{{ post.url }}">{{ post.title }}</a>
			<div class="date">
			<span>{{ post.date | date_to_string }}</span>
			</div>
		</h3>
	</div>
	<div class="post">
		<p>
		{{ post.excerpt }}
		</p>
		<p class="post-nav">
			<a href="{{ post.url }}">>>Read more</a>
		</p>
	</div>
	<div class="break"></div> 
</div>  
{% endfor %}