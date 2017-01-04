---
layout: page
title: NJOY Projects
---
NJOY21 is made up of many smaller projects. These projects each solve some problem or implement some bit of code. Here are the various projects that make up NJOY21:
<ul>
{% for project in site.data.projects.Projects %}
  <li>
     <a href="{{ project.url }}">{{ project.name }}</a> {{ project.description }}
  </li>
{% endfor %}
</ul>

## Supporting Projects
Some of the projects maintained by NJOY developers don't directly contribute to the NJOY21 source code, but are supporting materials such as the website and documentation. Here are those projects.
<ul>
{% for project in site.data.projects.Supporting %}
  <li>
     <a href="{{ project.url }}">{{ project.name }}</a> {{ project.description }}
  </li>
{% endfor %}
</ul>

## Third-Party Projects
NJOY21 utilizes a number of third-party code, code that was not developed directly for NJOY. We maintain our own "adapters" to those third-party repositories. Our adapters take the third-party code and adapts it for our build/test system. The third-party projects that we use are:
<ul>
{% for project in site.data.projects.ThirdParty %}
  <li>
     <a href="{{ project.url }}">{{ project.name }}</a> {{ project.description }}
  </li>
{% endfor %}
</ul>
