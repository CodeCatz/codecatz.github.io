---
layout: page
title: CodeCatz projects
---

{% assign current_projects = (site.posts | where: 'status', 'CURRENT') %}
{% assign completed_projects = (site.posts | where: 'status', 'DONE') %}

### Ongoing projects
<div class="break"></div>
{% for project in current_projects  %}
<div class="container-fluid section-posts">
	<h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
	<div>
		<a href="{{ project.repository }}" class="project-link" target="_blank"><i class="fa fa-code-fork"></i></a>
		{% if project.website %} <a href="{{ project.website }}" class="project-link" target="_blank"><i class="fa fa-globe"></i></a>{% endif %} 
		Technologies: {{ project.technologies }}
	</div>
	<div>Project started on: <span class="date">{{ project.start_date | date_to_string }}</span></div>
	<br/>
</div>  
{% endfor %}

### Completed projects
<div class="break"></div>
{% for project in completed_projects %}
<div class="container-fluid section-posts">
	<h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
	<div>
		<a href="{{ project.repository }}" class="project-link" target="_blank"><i class="fa fa-code-fork"></i></a>
		{% if project.website %} <a href="{{ project.website }}" class="project-link" target="_blank"><i class="fa fa-globe"></i></a>{% endif %} 
		Technologies: {{ project.technologies }}
	</div>
	<div>Project completed on: <span class="date">{{ project.end_date | date_to_string }}</span></div>
	<br/>
</div>  
{% endfor %}
