---
title: Fortschritt
layout: page
permalink: "/fortschritt/"
---

<div class="posts">
	{% for post in site.posts %}
  <article>
    {% if post.image %}
      <a href="#" class="image"><img src="{{ post.image | prepend: '/assets/images/' | prepend: site.baseurl | absolute_url }}" alt="" /></a>
    {% endif %}
    <h3>{{post.title}}</h3>
    <p>{{post.abstract}}</p>
    <ul class="actions">
      <li><a href="{{post.url}}" class="button">Read More</a></li>
    </ul>
  </article>
	{% endfor %}
</ul>
