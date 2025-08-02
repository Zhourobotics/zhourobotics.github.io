---
layout: page
permalink: /team/
title: Team
nav: true
nav_order: 3
---

## Faculty

<div class="row">
{% for person in site.data.faculty %}
<div class="col-sm-6 col-md-4 col-lg-3" style="margin-bottom: 20px;">
    <div class="text-center">
        <img class="img-fluid rounded" style="width: 150px; height: 150px; object-fit: cover; margin-bottom: 10px;" src="{{ person.image | prepend: '/assets/img/people/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
        <h5 style="margin-bottom: 3px;">
            {% if person.google_scholar %}
            <strong><a href="{{person.google_scholar}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.website %}
            <strong><a href="{{person.website}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.linkedin %}
            <strong><a href="https://www.linkedin.com/in/{{person.linkedin}}" target="_blank">{{person.name}}</a></strong>
            {% else %}
            <strong>{{person.name}}</strong>
            {% endif %}
        </h5>
        <p style="font-size: 0.9em; color: #666;">Assistant Professor</p>
        <!-- {% if person.email %}
        <small><i class="fa fa-envelope"></i> {{person.email}}</small>
        {% endif %} -->
    </div>
</div>
{% endfor %}
</div>

## PhD Students

<div class="row">
{% for person in site.data.phd_students %}
<div class="col-sm-6 col-md-4 col-lg-3" style="margin-bottom: 20px;">
    <div class="text-center">
        <img class="img-fluid rounded" style="width: 150px; height: 150px; object-fit: cover; margin-bottom: 10px;" src="{{ person.image | prepend: '/assets/img/people/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
        <h5 style="margin-bottom: 3px;">
            {% if person.google_scholar %}
            <strong><a href="{{person.google_scholar}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.website %}
            <strong><a href="{{person.website}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.linkedin %}
            <strong><a href="https://www.linkedin.com/in/{{person.linkedin}}" target="_blank">{{person.name}}</a></strong>
            {% else %}
            <strong>{{person.name}}</strong>
            {% endif %}
        </h5>
        {% if person.position contains 'Co-advised' %}
            {% if person.position contains 'Electrical and Computer Engineering' %}
            <p style="font-size: 0.9em; color: #666; margin-bottom: 2px;">ECE ({{person.position | split: '<br/>' | slice: 1, 1 | first | split: 'Drexel University,' | last | strip }} - )</p>
            <p style="font-size: 0.8em; color: #888; margin-top: 0; margin-bottom: 0;">{{person.position | split: '<br/>' | first | strip }}</p>
            {% elsif person.position contains 'Computer Science' %}
            <p style="font-size: 0.9em; color: #666; margin-bottom: 2px;">CS ({{person.position | split: '<br/>' | slice: 1, 1 | first | split: 'Drexel University,' | last | strip }} - )</p>
            <p style="font-size: 0.8em; color: #888; margin-top: 0; margin-bottom: 0;">{{person.position | split: '<br/>' | first | strip }}</p>
            {% endif %}
        {% elsif person.position contains 'Electrical and Computer Engineering' %}
        <p style="font-size: 0.9em; color: #666;">ECE ({{person.position | split: '<br/>' | first | split: 'Drexel University,' | last | strip }} - )</p>
        {% elsif person.position contains 'Computer Science' %}
        <p style="font-size: 0.9em; color: #666;">CS ({{person.position | split: '<br/>' | first | split: 'Drexel University,' | last | strip }} - )</p>
        {% else %}
        <p style="font-size: 0.9em; color: #666;">{{person.position | split: ',' | first | strip_html | truncate: 30}}</p>
        {% endif %}
        <!-- {% if person.email %}
        <small><i class="fa fa-envelope"></i> {{person.email}}</small>
        {% endif %} -->
    </div>
</div>
{% endfor %}
</div>

## Masters and Undergraduates

<div class="row">
{% for person in site.data.masters_undergraduates %}
<div class="col-sm-6 col-md-4 col-lg-3" style="margin-bottom: 20px;">
    <div class="text-center">
        <img class="img-fluid rounded" style="width: 150px; height: 150px; object-fit: cover; margin-bottom: 10px;" src="{{ person.image | prepend: '/assets/img/people/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
        <h5 style="margin-bottom: 3px;">
            {% if person.google_scholar %}
            <strong><a href="{{person.google_scholar}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.website %}
            <strong><a href="{{person.website}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.linkedin %}
            <strong><a href="https://www.linkedin.com/in/{{person.linkedin}}" target="_blank">{{person.name}}</a></strong>
            {% else %}
            <strong>{{person.name}}</strong>
            {% endif %}
        </h5>
        {% if person.degrees contains 'MS Student' %}
            {% if person.position contains 'Electrical and Computer Engineering' %}
            <p style="font-size: 0.9em; color: #666;">MS (ECE)</p>
            {% elsif person.position contains 'Computer Science' %}
            <p style="font-size: 0.9em; color: #666;">MS (CS)</p>
            {% elsif person.position contains 'Mechanical Engineering' %}
            <p style="font-size: 0.9em; color: #666;">MS (ME)</p>
            {% elsif person.position contains 'Robotics' %}
            <p style="font-size: 0.9em; color: #666;">MS (Robotics)</p>
            {% else %}
            <p style="font-size: 0.9em; color: #666;">MS</p>
            {% endif %}
        {% elsif person.degrees contains 'BE Student' or person.degrees contains 'BS Student' or person.degrees contains 'BTech Student' %}
            {% if person.name contains 'Satoru Eto' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (CD)</p>
            {% elsif person.name contains 'Logan Voravong' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (CS & Math)</p>
            {% elsif person.position contains 'Electrical and Computer Engineering' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (ECE)</p>
            {% elsif person.position contains 'Computer Science' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (CS)</p>
            {% elsif person.position contains 'Mechanical Engineering' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (ME)</p>
            {% elsif person.position contains 'Robotics' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (Robotics)</p>
            {% else %}
            <p style="font-size: 0.9em; color: #666;">Undergrad</p>
            {% endif %}
        {% else %}
        <p style="font-size: 0.9em; color: #666;">{{person.position | split: ',' | first | strip_html | truncate: 30}}</p>
        {% endif %}
        <!-- {% if person.email %}
        <small><i class="fa fa-envelope"></i> {{person.email}}</small>
        {% endif %} -->
    </div>
</div>
{% endfor %}
</div>

## Visiting Students

<div class="row">
{% for person in site.data.visiting_students %}
<div class="col-sm-6 col-md-4 col-lg-3" style="margin-bottom: 20px;">
    <div class="text-center">
        <img class="img-fluid rounded" style="width: 150px; height: 150px; object-fit: cover; margin-bottom: 10px;" src="{{ person.image | prepend: '/assets/img/people/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
        <h5 style="margin-bottom: 3px;">
            {% if person.google_scholar %}
            <strong><a href="{{person.google_scholar}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.website %}
            <strong><a href="{{person.website}}" target="_blank">{{person.name}}</a></strong>
            {% elsif person.linkedin %}
            <strong><a href="https://www.linkedin.com/in/{{person.linkedin}}" target="_blank">{{person.name}}</a></strong>
            {% else %}
            <strong>{{person.name}}</strong>
            {% endif %}
        </h5>
        {% if person.degrees contains 'Undergraduate Student' %}
            {% if person.name contains 'Katherine Song' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (EE, Northwestern)</p>
            {% elsif person.name contains 'Ava Bowman' %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (Math, Wesleyan)</p>
            {% else %}
            <p style="font-size: 0.9em; color: #666;">Undergrad (CE, UMich)</p>
            {% endif %}
        {% else %}
        <p style="font-size: 0.9em; color: #666;">{{person.position | strip_html | truncate: 30}}</p>
        {% endif %}
        <!-- {% if person.email %}
        <small><i class="fa fa-envelope"></i> {{person.email}}</small>
        {% endif %} -->
    </div>
</div>
{% endfor %}
</div>

## Alumni

{% for alum in site.data.alumni %}
<p style="margin-bottom: 8px;">
    {% if alum.website %}
    <strong><a href="{{alum.website}}" target="_blank">{{alum.name}}</a></strong>
    {% elsif alum.linkedin %}
    <strong><a href="https://www.linkedin.com/in/{{alum.linkedin}}" target="_blank">{{alum.name}}</a></strong>
    {% else %}
    <strong>{{alum.name}}</strong>
    {% endif %}
    {% if alum.previously and alum.now %}
    ({{alum.previously | strip_html | truncate: 40}}, Next: {{alum.now | strip_html | truncate: 40}})
    {% elsif alum.previously %}
    ({{alum.previously | strip_html | truncate: 40}})
    {% elsif alum.now %}
    (Next: {{alum.now | strip_html | truncate: 40}})
    {% endif %}
</p>
{% endfor %}

