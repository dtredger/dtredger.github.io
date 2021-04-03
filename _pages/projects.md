---
title:
layout: default
permalink: /projects/
published: true
---


<div class="ProjectContainer">
    <div class="gallery">
        {% for project in site.projects %}
            {% if project.redirect %}
                <div class="projectTile" style="background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
url({{ project.image | prepend: '/assets/images/' }}); background-size: cover;">
                    <a href="{{ project.redirect }}" target="_blank">
                        <span style="color:#aaa"><h2>{{ project.title }}</h2>
                            <br/>
                            <p>{{ project.description }}</p>
                        </span>
                    </a>
                </div>
            {% else %}
                <div class="projectTile" style="background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
url({{ project.image | prepend: '/assets/images/' }}); background-size: cover;">
                    <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
                        <span style="color:#aaa">
                          <h2>{{ project.title }}</h2>
                          <br/>
                          <p>{{ project.description }}</p>
                        </span>
                    </a>
                </div>
            {% endif %}

        {% endfor %}
    </div>
</div>
