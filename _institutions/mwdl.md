---
inst_code: mwdl
name: Mountain West Digital Library
description: "MWDL provides free access to over 960,000 resources from universities, colleges, public libraries, museums, historical societies, and government agencies, counties, and municipalities in Utah, Nevada, Idaho, Hawaii, and other parts of the U.S. West."
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