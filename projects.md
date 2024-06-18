---
title: projects
description: Some of the projects I've worked on
layout: default
show_github_link: false
---
{%include navbar.html%}

<table>
	<tr>
		<th colspan="3">Featured Projects</th>
	</tr>
	<tr>
		<th>
		Project Name
		</th>
		<th>
		Date Completed
		</th>
		<th>
		Project Description
		</th>
	</tr>
	{% for proj in site.data.projects %}
		{% if proj.featured %}
			<tr>
				<td>
					<a href="{{ proj.link }}">{{ proj.project-name }}</a>
				</td>
				<td>
					{{ proj.date }}
				</td>
				<td>
					{{ proj.desc }}
				</td>
			</tr>
		{% endif %}
	{% endfor %}
	<tr>
		<th colspan="3">Other Projects</th>
	</tr>
	<tr>
		<th>
		Project Name
		</th>
		<th>
		Date Completed
		</th>
		<th>
		Project Description
		</th>
	</tr>
	{% for proj in site.data.projects %}
		{% unless proj.featured %}
			<tr>
				<td>
					<a href="{{ proj.link }}">{{ proj.project-name }}</a>
				</td>
				<td>
					{{ proj.date }}
				</td>
				<td>
					{{ proj.desc }}
				</td>
			</tr>
		{% endunless %}
	{% endfor %}
</table>