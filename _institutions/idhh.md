---
inst_code: idhh
name: Illinois Digital Heritage Hub
description: "The Illinois Digital Heritage Hub is a collaboration between Illinois State Library, the Consortium of Academic and Research Libraries in Illinois, Chicago Public Library, and the University of Illinois at Urbana-Champaign."
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