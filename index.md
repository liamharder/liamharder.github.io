---
title: home
description: ePortfolio - Liam Harder
layout: default
show_github_link: true
---
# Liam Jakob Harder
### Coder - Creator - Collaborator
{%include navbar.html%}

intro paragraph

## Projects
project highlights go here
<table>
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
</table>

## Education
classes go here

<h2 id="contact">Contact</h2>
contact info