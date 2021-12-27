---
inst_code: nyarc
name: NYARC
description: "The New York Art Resources Consortium (NYARC) consists of the research libraries and archives of three leading art museums in New York City: The Brooklyn Museum, The Frick Collection, and The Museum of Modern Art. With funding from The Andrew W. Mellon Foundation, NYARC was formed in 2006 to facilitate collaboration that results in enhanced resources to research communities."
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