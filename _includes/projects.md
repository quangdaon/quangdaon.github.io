
{% assign sortedProjects = site.projects | sort: 'priority', 'last' %}
{% for project in sortedProjects %}
## {{ project.title }}

{{ project.description }}

{% for link in project.links %}
<a class="button button-1" href="{{ link.url }}" target="_blank" rel="noopener"><i class="fa fa-{{ link.icon}} fa-md"></i> {{ link.label }}</a>
{% endfor %}

{% endfor %}