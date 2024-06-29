---
title: home
description: The ePortfolio of Liam Harder
layout: default
show_github_link: true
---
# Liam Jakob Harder
### Coder - Creator - Collaborator
{%include navbar.html%}

Hello, and welcome to my ePortfolio! If you're reading this, it's most likely because I've applied for a position with your organization. If that's the case, please allow me to show you the skills and experience I can bring to the job, along with some of my previous work. Thank you for your consideration, and I hope to hear from you soon!

## Projects
Below are some examples of what I consider to be my finest work across a number of courses and disciplines. A more complete list of projects I've completed can be found on the Projects page.
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
As of June 2024, I am in my 5th year of studies towards a Bachelor of Technology degree from Kwantlen Polytechnic University, majoring in Information Technology. Academically, I am in my 4th year, having completed the majority of my 3rd year courses. As with everyone else, the COVID-19 pandemic significantly disrupted my studies (along with every other aspect of my daily life), but even in the face of adversity I am proud to have maintained a cumulative GPA of 4.05 - my stride may have slowed, but it has not faltered. I have also demonstrated an ability to learn new skills and develop new competencies quickly and efficiently, as evidenced by my high grades in several classes outside my primary discipline of IT. A list of my most relevant courses can be found below; more information is available on the Education page.

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
</table>

<h2 id="contact">Contact</h2>
If you want to get in touch with me to arrange an interview or for any other reason, I can be found on:

[LinkedIn](https://www.linkedin.com/in/liam-j-harder/)

[GitHub](https://github.com/liamharder)

Email - [liamharder06@gmail](mailto:liamharder06@gmail)