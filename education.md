---
title: education
description: A summary of my post-secondary studies
layout: default
show_github_link: false
---
{%include navbar.html%}

<table>
	<tr>
		<th colspan="3"><h1 style="color: #b5e853; text-align: center">Featured Courses</h1></th>
	</tr>
	{% for course in site.data.courses %}
		{% if course.featured %}
			<tr>
				<td>
					Name: {{ course.class }}
				</td>
				<td>
					Date Complete: {{ course.date }}
				</td>
			</tr>
			<tr>
				<td colspan="2">
					Description: {{ course.desc }}
					<br>
					Final Grade: {{ course.grade}}
				</td>
			</tr>
		{% endif %}
	{% endfor %}
	<tr>
		<th colspan="3"><br><br><br><h1 style="color: #b5e853; text-align: center">Other Courses</h1></th>
	</tr>
	{% for course in site.data.courses %}
		{% unless course.featured %}
			<tr>
				<td>
					Name: {{ course.class }}
				</td>
				<td>
					Date Complete: {{ course.date }}
				</td>
			</tr>
			<tr>
				<td colspan="2">
					Description: {{ course.desc }}
					<br>
					Final Grade: {{ course.grade}}
				</td>
			</tr>
		{% endunless %}
	{% endfor %}
</table>