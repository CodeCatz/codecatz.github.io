---
layout: default
title: CodeCatz projects
---

{% assign current_projects = (site.posts | where: 'status', 'CURRENT') %}
{% assign completed_projects = (site.posts | where: 'status', 'DONE') %}
<div class="page-dscr">
	<h2>Ongoing projects</h2>
	{% for project in current_projects  %}
	<div class="container-fluid section-posts">
		<div class="meetup">
			<h2><a href="{{ project.url }}">{{ project.title }}</a></h2>
		</div>
		<div>Project lead: <a href="https://github.com/{{ project.project_lead }}" target="_blank">{{ project.project_lead }}</a></div>
		<div>Project started on: <span class="date">{{ project.start_date | date_to_string }}</span></div>
		<div class="break"></div> 
	</div>  
	{% endfor %}
	<h2>Completed projects</h2>
	{% for project in completed_projects %}
	<div class="container-fluid section-posts">
		<div class="meetup">
			<h2><a href="{{ project.url }}">{{ project.title }}</a>
			</h2>
			<div>Project completed on: <span class="date">{{ project.end_date | date_to_string }}</span></div>
		</div>
		<div class="break"></div> 
	</div>  
	{% endfor %}
</div>