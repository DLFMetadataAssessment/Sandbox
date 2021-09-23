---
inst_code: odn
name: Ohio Digital Network
description: "Led by the State Library of Ohio and in partnership with Ohio Library and Information Network, Ohio Public Library Information Network, and Ohio History Connection, the Ohio Digital Network builds on strong digital collection efforts across the state including Ohio Memory and the Ohio Digitization Hubs project."
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