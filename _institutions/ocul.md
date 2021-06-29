---
inst_code: ocul
name: OCUL--Scholars Portal
description: "Scholars Portal is a service of the Ontario Council of University Libraries (OCUL). Founded in 2002, Scholars Portal provides a shared technology infrastructure and shared collections for all 21 university libraries in the province."
---

<h1>{{ page.name }}</h1>

{{ page.description }}

<ul>
    {% for spec in site.metadata_specs %}
        {% if spec.institution == page.inst_code %}
            <li>
                <h2><a href="{{ spec.url}}">{{ spec.title }}</a></h2>
                <p>{{ spec.description }}</p>
            </li>
        {% endif %}
    {% endfor %}
</ul>