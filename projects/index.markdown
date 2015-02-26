---
layout: default
title: CodeCatz projects
---

{% assign current_projects = (site.posts | where: 'status', 'CURRENT') %}
{% assign completed_projects = (site.posts | where: 'status', 'DONE') %}
<div class="page-dscr">
	<h2>Ongoing projects</h2>
	<div class="break"></div>
	{% for project in current_projects  %}
	<div class="container-fluid section-posts">
		<h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
		<div><a href="{{ project.repository }}" class="project-link" target="_blank"><i class="fa fa-code-fork"></i></a>{% if project.website %} <a href="{{ project.website }}" class="project-link" target="_blank"><i class="fa fa-globe"></i></a>{% endif %} Technologies: {{ project.technologies }} | Project lead: <a href="https://github.com/{{ project.project_lead }}"  target="_blank">{{ project.project_lead }}</a></div>
		<div>Project started on: <span class="date">{{ project.start_date | date_to_string }}</span></div>
		{% if page.end_date %}<div>Project ended on: <span class="date">{{ page.end_date | date_to_string }}</span></div>{% endif %}
	</div>  
	{% endfor %}
	<h2>Completed projects</h2>
	<div class="break"></div>
	{% for project in completed_projects %}
	<div class="container-fluid section-posts">
		<div class="meetup">
			<h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
			<div><a href="{{ project.repository }}" class="project-link" target="_blank"><i class="fa fa-code-fork"></i></a>{% if project.website %} <a href="{{ project.website }}" class="project-link" target="_blank"><i class="fa fa-globe"></i></a>{% endif %} Technologies: {{ project.technologies }} | Project lead: <a href="https://github.com/{{ project.project_lead }}"  target="_blank">{{ project.project_lead }}</a></div>
			<div>Project completed on: <span class="date">{{ project.end_date | date_to_string }}</span></div>
		</div>
	</div>  
	{% endfor %}
</div>