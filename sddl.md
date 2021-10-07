---
inst_code: south-dakota-digital-library
name: South Dakota Digital Library
description: "The Digital Library of South Dakota (DLSD) is a collaboration of the libraries of the six Board of Regents colleges and universities as well as partners in the state of South Dakota."
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