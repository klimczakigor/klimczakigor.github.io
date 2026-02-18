---
layout: page
title: Lecture Notes
includelink: true
nav_order: 2
---

Lecture notes and write-ups.

{% assign lecture_posts = site.posts | where_exp: "post", "post.tags contains 'lecture-notes'" %}

{% if lecture_posts.size > 0 %}
<ul class="card-list">
  {% for post in lecture_posts %}
    <li class="post-card">
      <div class="badge">Post</div>
      <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html }}</p>
      {% assign words = post.content | number_of_words %}
      {% assign minutes = words | divided_by: 200 | plus: 1 %}
      <div class="card-meta">{{ post.date | date: "%B %-d, %Y" }} · {{ minutes }} min</div>
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="muted">No lecture notes yet.</p>
{% endif %}
