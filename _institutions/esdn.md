---
inst_code: esdn
name: Empire State Digital Network
description: "Empire State Digital Network is a service hub of the Digital Public Library of America (DPLA). The Network is administered by the Metropolitan New York Library Council (METRO) in collaboration with eight allied regional library councils collectively working as the Empire State Library Network."
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