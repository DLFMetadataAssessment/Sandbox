---
inst_code: carnegie-hall
name: Carnegie Hall Archives
description: "Carnegie Hall's mission is to present extraordinary music and musicians on the three stages of this legendary hall, to bring the transformative power of music to the widest possible audience, to provide visionary education programs, and to foster the future of music through the cultivation of new works, artists and audiences. The Carnegie Hall Archives' mission is to acquire, preserve, and make publicly accessible documents and materials—physical and digital—related to the origins, history, activities, growth, and development of Carnegie Hall."
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
