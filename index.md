---
layout: default
title: "Home"
---

# Welcome to My Blog

This is my personal blog where I share thoughts and ideas. Stay tuned for more posts!

## Latest Posts

{% for post in site.posts %}
  <div class="card mb-4">
    <div class="card-body">
      <h5 class="card-title"><a href="{{ post.url }}">{{ post.title }}</a></h5>
      <p class="card-text">{{ post.excerpt | strip_html }}</p>
      <a href="{{ post.url }}" class="btn btn-primary">Read More</a>
    </div>
  </div>
{% endfor %}
