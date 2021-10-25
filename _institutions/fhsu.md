---
inst_code: fhsu
name: Fort Hays State University
description: "Forsyth Library is the main library of Fort Hays State University."
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