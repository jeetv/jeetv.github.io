---
layout: page
title: Projects
permalink: /projects/
description: (Project page Work in Progress.....)
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

<div class="container-fluid mt-3;">
  <div class="row">
    <div class="col-md-6 mb-4">
      <div class="ratio ratio-16x9">
        {% include video.liquid 
            path="https://www.youtube.com/embed/7RRSzT9xw5g?si=jxhU-wv1ML2udKDC" 
            class="rounded z-depth-1"
            width="100%"
            height="250"
        %}
      </div>
      <div class="caption mt-2 text-center">
        Bringing Generalization to Deep Multi-View Pedestrian Detection - RWS @ WACV2023 - Oral presentation
      </div>
    </div>
    <div class="col-md-6 mb-4">
      <div class="ratio ratio-16x9">
        {% include video.liquid 
            path="https://www.youtube.com/embed/yuYv7DA-H8w?si=Uuo41Y3nwnOwSkqC" 
            class="rounded z-depth-1"
            width="100%"
            height="250"
        %}
      </div>
      <div class="caption mt-2 text-center">
        CVIT Lab, IIIT-Hyderabad R&D Showcase <br>
        Multi Camera Pedestrian Detection and Tracking <br>
        (GMVD Dataset samples, Cricket Player Tracking demo)
      </div>
    </div>
    </div>
    <div class="row">
    <div class="col-md-6 mb-4">
      <div class="ratio ratio-16x9">
        {% include video.liquid 
            path="https://www.youtube.com/embed/AaWtbsLU7Bk?si=Mdor2WhRGPJgqxNZ" 
            class="rounded z-depth-1"
            width="100%"
            height="250"
        %}
      </div>
      <div class="caption mt-2 text-center">
        Apple Iphone Assembly PoC - CVIT Lab, IIIT-Hyderabad  <br>
        Video Action/Activity Recognition for industrial assembly operations.
      </div>
    </div>
    <div class="col-md-6 mb-4">
      <div class="ratio ratio-16x9">
        {% include video.liquid 
            path="https://www.youtube.com/embed/xGcqd0jVJ4o?si=qL-siAls6QzySiqm"
            class="rounded z-depth-1"
            width="100%"
            height="250"
        %}
      </div>
      <div class="caption mt-2 text-center">
        Multi-Camera Background Subtracted Pedestrian and <br> Occupancy Map Projection
      </div>
    </div>
  </div>
</div>

<div class="projects">

  {% if site.enable_project_categories and page.display_categories %}
    <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <a id="{{ category }}" href=".#{{ category }}">
        <h2 class="category" style="text-align: left; font-weight: bold;"><strong>{{ category }}</strong></h2>
      </a>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-1 row-cols-md-2">
            {% for project in sorted_projects %}
              {% include projects_horizontal.liquid %}
            {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="row row-cols-1 row-cols-md-3">
          {% for project in sorted_projects %}
            {% include projects.liquid %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}
  {% else %}
    <!-- Display projects without categories -->
    {% assign sorted_projects = site.projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.liquid %}
          {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="row row-cols-1 row-cols-md-3">
        {% for project in sorted_projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% endif %}
  {% endif %}
</div>
