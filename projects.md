---
title: projects
description: Some of the projects I've worked on
layout: default
show_github_link: false
---
{%include navbar.html%}

<table>
	<tr>
		<th colspan="3"><h1 style="color: #b5e853; text-align: center">Featured Projects</h1></th>
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
			<tr>
				---
			</tr>
		{% endif %}
	{% endfor %}
	<tr>
		<th colspan="3"><br><br><br><h1 style="color: #b5e853; text-align: center">Other Projects</h1></th>
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
			<tr>
				---
			</tr>
		{% endunless %}
	{% endfor %}
</table>