---
layout: page
title: About CodeCatz
---

CodeCatz is a coding study group where women are never in the minority. We hack open source projects together and participate in cool tech events.

The idea for CodeCatz was born at the [Girls After Rails Meetup](https://www.facebook.com/events/456717001084428/) in Summer 2013. The first CodeCatz meetup took place on Wednesday, July 17 at the offices of <a href="http://www.zemanta.com">Zemanta</a>. Since then, we have been meeting every Wednesday at different locations around Ljubljana. Our hosts also included <a href="http://www.celtra.com">Celtra</a> and <a href="http://hekovnik.si">Hekovnik</a>. In July 2014, we made ourselves at home at <a href="https://www.facebook.com/rampalab/">RAMPA Lab</a>, where we had regular meetups up until the end of 2015. Now we mostly work together online.

<a href="http://visual.ly/codecatz-year-review-2014">2014 was quite a year for us</a>! We developed, released and mainted our first big common project, the events website for <a href="http://codeweek.eu">Europe Code Week</a>. We also organized several beginner programming workshops for women, spoke at different events, and were nominated for person of the year 2014 by Delo.

## Who's behind CodeCatz?

CodeCatz is a group volunteering effort. Currently active Catz:

- Alja Isaković (<a href="https://twitter.com/ialja" target="_blank">@iAlja</a>)
- Erika Pogorelc (<a href="https://twitter.com/ercchy" target="_blank">@ercchy</a>)
- Mateja Verlič (<a href="https://twitter.com/sparkica" target="_blank">@sparkica</a>)
- Heidi Pungartnik (<a href="https://twitter.com/design4founders" target="_blank">@design4founders</a>)

## Projects

{% assign current_projects = (site.posts | where: 'status', 'CURRENT' | sort: 'start_date') %}
{% assign completed_projects = (site.posts | where: 'status', 'DONE' | sort: 'end_date') %}

Current projects:

<ul>
{% for project in current_projects reversed %}
	<li>{% if project.website %} <a href="{{ project.website }}" target="_blank">{{ project.title }}</a>{% else %}{{ project.title }}{% endif %} | {{ project.technologies }} <a href="{{ project.repository }}" target="_blank"><i class="fa fa-code-fork"></i></a>
	</li>
{% endfor %}
</ul> 

Completed projects:
<ul>
{% for project in completed_projects reversed %}
	<li>{% if project.website %} <a href="{{ project.website }}" target="_blank">{{ project.title }}</a>{% else %}{{ project.title }}{% endif %} | {{ project.technologies }}, {{ project.end_date | date: "%B %Y" }} <a href="{{ project.repository }}" target="_blank"><i class="fa fa-code-fork"></i></a>
	</li>
{% endfor %}
</ul>  

## Press

{% assign sorted_mentions = site.data.press | sort: 'date' %}
{% for mention in sorted_mentions reversed %}
- <a href="{{ mention.url }}" target="_blank">{{ mention.title }}</a> ({{ mention.date | date: "%B %Y" }})
{% endfor %}

