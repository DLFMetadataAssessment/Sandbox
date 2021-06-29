---
inst_code: usu
name: Utah State University Libraries
description: "The Utah State University Libaries include Merill-Cazier Library, the USU Eastern Price and USU Eastern Blanding campus libraries, the Anne Carroll Moore Library of the Edith Bowen Laboratory School, the Young Education Technology Center, the Intermountain Herbarium and the Quinney Natural Resources Library in the Quinney College of Natural Resources."
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