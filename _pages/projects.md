---
layout: page
title: projects
permalink: /projects/
description: This is a collection of research and class projects I am either working on or completed.
nav: true
---

<div class="projects grid">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            <div class="col-4">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if project.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ project.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
            {% if project.bitbucket %}
              <div class="github-icon">
                <div class="icon" data-toggle="tooltip" title="Code Repository">
                  <a href="{{ project.bitbucket }}" target="_blank"><i class="fab fa-bitbucket gh-icon"></i></a>
                </div>
              </div>
            {% endif %}
            </div>
            <div class="col-8">
            {% for tag in project.tags %}
              <div class="github-icon float-right">
                <div class="icon" data-toggle="tooltip" title="{{ tag }}">
                  <i class="fab devicon-{{ tag }}-plain colored"></i>
                </div>
              </div>
            {% endfor %}
            </div>
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
