---
layout: page
title: CodeCatz projects
---

{% assign current_projects = (site.posts | where: 'status', 'CURRENT' | sort: 'start_date') %}
{% assign completed_projects = (site.posts | where: 'status', 'DONE' | sort: 'end_date') %}

### Ongoing projects
<div class="break"></div>
{% for project in current_projects reversed %}
<div class="container-fluid section-posts">
	<h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
	<div>
		<a href="{{ project.repository }}" class="project-link" target="_blank"><i class="fa fa-code-fork"></i></a>
		{% if project.website %} <a href="{{ project.website }}" class="project-link" target="_blank"><i class="fa fa-globe"></i></a>{% endif %} 
		Technologies: {{ project.technologies }}
	</div>
	<div>Project started in <span class="date">{{ project.start_date | date: "%B %Y" }}</span></div>
	<br/>
</div>  
{% endfor %}

### Completed projects
<div class="break"></div>
{% for project in completed_projects reversed %}
<div class="container-fluid section-posts">
	<h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
	<div>
		<a href="{{ project.repository }}" class="project-link" target="_blank"><i class="fa fa-code-fork"></i></a>
		{% if project.website %} <a href="{{ project.website }}" class="project-link" target="_blank"><i class="fa fa-globe"></i></a>{% endif %} 
		Technologies: {{ project.technologies }}
	</div>
	<div>Project completed in <span class="date">{{ project.end_date | date: "%B %Y" }}</span></div>
	<br/>
</div>  
{% endfor %}
