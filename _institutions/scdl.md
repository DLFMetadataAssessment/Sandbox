---
inst_code: scdl
name: South Carolina Digital Library
description: "The South Carolina Digital Library provides free access to historic materials illustrating the history and culture of South Carolina from over 40 cultural heritage institutions across the state."
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