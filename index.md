---
title: Singularity
keywords: containers,
sidebar: main_sidebar
permalink: index.html
toc: false
---

Singularity enables users to have full control of their environment. This means that a non-privileged user can "swap out" the operating system on the host for one they control. So if the host system is running RHEL6 but your application runs in Ubuntu, you can create an Ubuntu image, install your applications into that image, copy the image to another host, and run your application on that host in it's native Ubuntu environment!


<a target="_blank" class="btn btn-primary navbar-btn cursorNorm" role="button" href="https://goo.gl/forms/D7ed1dfLeNvml6no1">Register your Cluster</a> <a target="_blank" href="https://goo.gl/forms/tGBKnKwplNyRZRSm2" class="btn btn-primary navbar-btn cursorNorm" role="button">Add a Publication</a>


Singularity also allows you to leverage the resources of whatever host you are on. This includes HPC interconnects, resource managers, file systems, GPUs and/or accelerators, etc. Singularity does this by enabling several key facets:

* Encapsulation of the environment
* Containers are image based
* No user contextual changes or root escalation allowed
* No root owned daemon processes

## Getting started

Jump in and <a href="/quickstart"><strong>get started</strong></a>.

<hr style="margin-top:20px">

<div class="row">
  {% assign loopcount = 1 %}
  {% for post in site.posts %}

   {% if loopcount < 4 %}

   <!-- Parse news-->
   {% if post.category == "news" %}
   {% assign loopcount = loopcount | plus: 1 %}
   <div class="col-md-4">
      <h2><a class="post-link" href="{{ post.url | remove: "/" }}">{{ post.title }}</a></h2>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <p>{{ post.content | truncatewords: 20 | strip_html }}</p>  
   </div>
   {% endif %}

   {% if post.category == "releases" %}
   {% assign loopcount = loopcount | plus: 1 %}
   <div class="col-md-4">
      <h2><a class="post-link" href="{{ post.url | remove: "/" }}">{{ post.title }}</a></h2>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <p>{{ post.content | truncatewords: 20 | strip_html }}</p>  
   </div>
   {% endif %}
   {% endif %}

  {% endfor %}
</div>
