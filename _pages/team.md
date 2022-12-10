---
layout: page
permalink: /team/
title: Team
nav: true
nav_order: 3
---

{% for person in site.data.members %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{person.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px; padding-left: 10px">
    <img class="img-fluid" style="float: left; width: auto; padding-left: 5px; padding-right: 20px; min-width: 100px; max-height: 185px; padding-bottom: 10px" src="{{ person.image | prepend: '/assets/img/people/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
    <div>
        <h4>{{person.name}}{% if person.degrees %}, {{person.degrees}} {% endif %}</h4>
        {{person.position | markdownify}}
        <i class="fa fa-envelope"></i> <em>{{person.email}}</em> <br>
        {% if person.website %}
          <i class="fa fa-globe"></i> <a href= "{{person.website}}" target="_blank"> @{{person.name}}</a> <br>
        {% endif %}        
        {% if person.twitter %}
          <i class="fab fa-twitter"></i> <a href= "http://twitter.com/{{person.twitter}}" target="_blank"> @{{person.twitter}} </a> <br>
        {% endif %}
        {% if person.linkedin %}
          <i class="fab fa-linkedin"></i> <a href= "https://www.linkedin.com/in/{{person.linkedin}}" target="_blank"> @{{person.name}} </a> <br>
        {% endif %}
        {% if person.github %}
          <i class="fab fa-github"></i> <a href= "https://github.com/{{person.github}}" target="_blank"> {{person.github}} </a> <br>
        {% endif %}
        {% if person.scholar %}
          <i class="ai ai-google-scholar"></i> <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"> Scholar Citations </a> <br>
        {% endif %}
        {% if person.orcid %}
          <i class="ai ai-orcid"></i> <a href="http://{{person.orcid}}" target="_blank"> {{person.orcid}}</a> <br>
        {% endif %} <br>
        {{person.description}} 
        {{person.description1| markdownify}}
    </div>
<!--     <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div> -->
</div>
<hr>
{% endfor %}


{% if site.data.affiliates %}
  <h2>affiliate members</h2>
  {% for person in site.data.affiliates %}
<div id = "{{person.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <img style="float: right; width: 42%; padding-left: 20px;" src="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{person.name}}">
    <div>
        <h4>{{person.name}}{% if person.degrees %}, {{person.degrees}} {% endif %}</h4>
        {{person.position}} <br>
        <i class="fa fa-envelope"></i> <em>{{person.email}}</em> <br>
        {% if person.twitter %}
          <i class="fab fa-twitter"></i> <a href= "http://twitter.com/{{person.twitter}}" target="_blank"> @{{person.twitter}} </a> <br>
        {% endif %}
        {% if person.website %}
          <i class="fa fa-globe"></i> <a href= "{{person.website}}" target="_blank">{{person.website}}</a> <br>
        {% endif %}
        {% if person.github %}
          <i class="fab fa-github"></i> <a href= "https://github.com/{{person.github}}" target="_blank"> {{person.github}} </a> <br>
        {% endif %}
        {% if person.scholar %}
          <i class="ai ai-google-scholar"></i> <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"> Scholar Citations </a> <br>
        {% endif %}
        {% if person.orcid %}
          <i class="ai ai-orcid"></i> <a href="http://{{person.orcid}}" target="_blank"> {{person.orcid}}</a> <br>
        {% endif %}

    </div>
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
  {% endfor %}
{% endif %}


<!-- ## students -->
{% for student in site.data.students %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{person.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
  <strong>{{student.name}}{% if student.degrees %}, {{student.degrees}} {% endif %}</strong> <br>
  {{student.position}} <br>
  <i class="fa fa-envelope"></i> <em>{{student.email}}</em> <br>
  {% if student.description %}
  <div style="margin-left: 2.5em; padding-top: 8px; padding-bottom: 5px; ">{{student.description}}</div>
  {% else %}
  {% for paper in site.data.publications %}
  {% if paper.authors contains student.pubmed_name %}
  <div style="margin-left: 2.5em; padding-top: 8px; padding-bottom: 5px; ">{{paper.authors | remove: '**'}} <a href="/papers/index.html#{{paper.title}}">{{paper.title}}</a> {{paper.details}}</div>
  {% endif %}
  {% endfor %}
  {% endif %}
</div>

{% endfor %}


## Students working with us
{% for alum in site.data.omembers %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<!-- <div id = "{{alum.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px; padding-bottom: 20px;"> -->
  <strong>{{alum.name}}{% if alum.degrees %}, {{alum.degrees}} {% endif %}</strong> <br>
  {{alum.degree1}}<br>
  {{alum.degree2}}<br>
  {% if alum.website %} <i class="fa fa-globe"></i> <a href= "{{alum.website}}" target="_blank">@{{alum.name}}</a>  {% endif %}

  {% if alum.linkedin %}
    <i class="fab fa-linkedin"></i> <a href= "https://www.linkedin.com/in/{{alum.linkedin}}" target="_blank">@{{alum.name}} </a> <br>
  {% endif %}

  {% for paper in site.data.publications %}
  {% if paper.authors contains alum.pubmed_name %}
  <div style="margin-left: 2.5em; padding-top: 8px; padding-bottom: 5px; ">{{paper.authors | remove: '**'}} <a href="/papers/index.html#{{paper.title | replace: ' ', '-' |  remove: '.'}}">{{paper.title}}</a> {{paper.details}}</div>
  {% endif %}
  {% endfor %}
<!-- </div> -->
{% endfor %}

<!-- --- -->

<!-- ## collaborators -->

<!-- {% for collaborator in site.data.collaborators %}
- <strong>{{collaborator.name}}{% if collaborator.degrees %}, {{collaborator.degrees}} {% endif %}</strong>
  {{collaborator.position}}
  {% if collaborator.website %} <i class="fa fa-globe"></i> <a href= "{{collaborator.website}}" target="_blank">{{collaborator.website}}</a>  {% endif %}
{% endfor %} -->

