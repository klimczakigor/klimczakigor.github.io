---
layout: page
title: Muon
includelink: true
---

Notes and posts tagged with “muon”.

{% assign muon_posts = site.posts | where_exp: "post", "post.tags contains 'muon'" %}

{% if muon_posts.size > 0 %}
<ul class="card-list">
  {% for post in muon_posts %}
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
<p class="muted">No muon posts yet.</p>
{% endif %}
