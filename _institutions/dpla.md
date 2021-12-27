---
inst_code: dpla
name: Digital Public Library of America
description: "The Digital Public Library of America brings together the riches of America's libraries, archives, and museums, and makes them freely available to the world."
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