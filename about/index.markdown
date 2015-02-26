---
layout: default
title: About CodeCatz
---

<div class="container-fluid cover-about">
	<div class="row">
		<div class="col-md-12">
			<div class="page-dscr">
				<p>CodeCatz is a coding study group where women are never in the minority. We meet every Wednesday and hack open source projects together because we think that's fun and because we like learning.</p>
				<p>The idea for CodeCatz was born at the <a href="https://www.facebook.com/events/456717001084428/">Girls After Rails Meetup</a> in Summer 2013. The first CodeCatz meetup took place on Wednesday, July 17 at the offices of <a href="http://www.zemanta.com">Zemanta</a>. Since then, we have been meeting every Wednesday at different locations around Ljubljana. Our hosts also included <a href="http://www.celtra.com">Celtra</a> and <a href="http://hekovnik.si">Hekovnik</a>. In July 2014, we made ourselves at home at <a href="https://www.facebook.com/rampalab/">RAMPA Lab</a>, where we still meet every Wednesday from 17:30-ish onwards.</p>
				<p><a href="http://visual.ly/codecatz-year-review-2014">2014 was quite a year for us</a>! We developed, released and mainted our first big common project, the events website for <a href="http://codeweek.eu">Europe Code Week</a>. We also organized several beginner programming workshops for women, spoke at different events, and were nominated for person of the year 2014 by Delo.</p>
				<h2>Who's behind CodeCatz?</h2>
				<p>CodeCatz is a group volunteering effort. The project is led by the following Catz (in alphabetical order):</p> 
				<ul>
					<li>Alja Isaković (<a href="https://twitter.com/ialja" target="_blank">@iAlja</a>)</li>
					<li>Erika Pogorelc (<a href="https://twitter.com/ercchy" target="_blank">@ercchy</a>)</li>
					<li>Goran Blažič (<a href="https://twitter.com/goranche" target="_blank">@goranche</a>)</li>
					<li>Jure Čuhalev (<a href="https://twitter.com/gandalfar" target="_blank">@gandalfar</a>)</li>
					<li>Mateja Verlič (<a href="https://twitter.com/sparkica" target="_blank">@sparkica</a>)</li>
				</ul>
				<h2>Press</h2>
				<ul>
					{% assign sorted_mentions = site.data.press | sort: 'date' %}
					{% for mention in sorted_mentions reversed %}
						<li><a href="{{ mention.url }}" target="_blank">{{ mention.title }}</a> ({{ mention.date | date: "%B %Y" }})</li>
					{% endfor %}
				</ul>
			</div>
		</div>
		<div class="col-md-8">
			<img class="illu-about" src="/assets/images/illustrations/catz_front_fill.png" >
		</div>
	</div>
</div>