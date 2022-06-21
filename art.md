---
layout: guide
ignore: true
title: Art
meta: "Art for research projects"
---
Sometimes, I draw art for research projects! Below is a collection of things I've drawn.

Are you a graduate student? Do you want me to draw something for your research project?
Send me an email at <span class="email-wrapper"><img class="email" src="/assets/email.svg" alt="vivian at eecs dot berkeley dot edu"></span>.

{% for a in site.data.art %}
<div class="project">
    <div class= "art">
        <img src="/assets/art/{{ a.img}}" class="art">
    </div>
    <div class="info">
    {% if a.project.link != nil %}
        <a href="{{ a.project.link }}" target="_blank">{{ a.project.name }}</a>
    {% else %}
        {{ a.project.name }}
    {% endif %}
        <br>
        {{ a.project.authors }}
        <br>
        {{ a.project.conference }}
    {% if a.note != nil %}
        <br>
        {{ a.note }}
    {% endif %}
    </div>
</div>
{% endfor %}
