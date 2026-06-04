---
layout: default
permalink: /en/blog/
title: blog
nav: false
pagination:
  enabled: true
  collection: en_posts
  sort_field: 'date'
  sort_reverse: true
  per_page: 10
---

<div class="post">

<ul class="post-list">
  {% for post in paginator.posts %}
  <li>
    {% assign content = post.content %}

    {% if content contains '<img src="' %}
      {% assign src = content | split: '<img src="' %}
      {% assign src = src[1] | split: '"' | first %}

      <div class="row align-items-center">
        <div class="col-sm-3">
            <img src="{{ src }}" class="rounded img-fluid z-depth-1" style="object-fit: cover; width: 100%; height: 150px;"/>
        </div>
        <div class="col-sm-9">
             <h3>
              <a class="post-title" href="{{ post.url | relative_url }}">
                {{ post.title }}
              </a>
            </h3>
            <p class="post-meta">
              <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
            </p>
            <div class="post-content">
              {{ post.content | strip_html | strip_newlines | strip | truncate: 200 }}
            </div>
        </div>
      </div>
    {% else %}
    <h3>
      <a class="post-title" href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </h3>
    <p class="post-meta">
      <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
    </p>

    <div class="post-content">
      {{ post.content | strip_html | strip_newlines | strip | truncate: 300 }}
    </div>
    {% endif %}
    
  </li>
  {% endfor %}
</ul>

{% include pagination.html %}

</div>
