---
layout: default
title: Home
permalink: /
---

<div class="row">
  {% for post in site.posts %}
    <div class="col-md-4">
      <div class="card mb-4">
        {% if post.featured_image %}
          <img src="{{ post.featured_image }}" class="card-img-top" alt="{{ post.title }}">
        {% endif %}
        <div class="card-body">
          <h5 class="card-title">{{ post.title }}</h5>
          <p class="card-text">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
          <a href="{{ post.url }}" class="btn btn-primary">Read More</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="btn btn-secondary">Previous</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="btn btn-secondary">Next</a>
  {% endif %}
</div>
