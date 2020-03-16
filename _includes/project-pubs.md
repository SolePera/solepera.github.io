{% assign project_pubs = site.pubs | where: 'project', include.project %}
{% for pub in project_pubs reversed %}
{{pub.excerpt | replace: "#", pub.url }}
{% endfor %}