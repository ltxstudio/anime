---
layout: default
title: "Home"
---

<div class="hero bg-primary text-white text-center py-5">
  <h1>Welcome to My Blog!</h1>
  <p class="lead">Discover articles on technology, design, and more.</p>
  <a href="/about/" class="btn btn-light btn-lg">Learn More</a>
</div>

# Latest Posts

<div class="row">
  {% for post in site.posts %}
    <div class="col-lg-4 col-md-6 col-sm-12 mb-4">
      <div class="card">
        <img src="{{ site.url }}/assets/images/default-thumbnail.jpg" class="card-img-top" alt="{{ post.title }}">
        <div class="card-body">
          <h5 class="card-title"><a href="{{ post.url }}">{{ post.title }}</a></h5>
          <p class="card-text">{{ post.excerpt | strip_html }}</p>
          <a href="{{ post.url }}" class="btn btn-primary">Read More</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="btn btn-outline-primary">Previous</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="btn btn-outline-primary">Next</a>
  {% endif %}
</div>
