---
layout: page
title: NJOY Components
---
NJOY21 is made up of many smaller components. These components each solve some problem or implement some bit of code. Here are the various components that make up NJOY21:
<ul>
{% for project in site.data.components.Components %}
  <li>
     <a href="{{ project.url }}">{{ project.name }}</a> {{ project.description }}
  </li>
{% endfor %}
</ul>

## Supporting Components
Some of the components maintained by NJOY developers don't directly contribute to the NJOY21 source code, but are supporting materials such as the website and documentation. Here are those components:
<ul>
{% for project in site.data.components.Supporting %}
  <li>
     <a href="{{ project.url }}">{{ project.name }}</a> {{ project.description }}
  </li>
{% endfor %}
</ul>

## Third-Party Components
NJOY21 utilizes a number of third-party code, code that was not developed directly for NJOY. We maintain our own "adapters" to those third-party repositories. Our adapters take the third-party code and adapts it for our build/test system. The third-party components that we use are:
<ul>
{% for project in site.data.components.ThirdParty %}
  <li>
     <a href="{{ project.url }}">{{ project.name }}</a> {{ project.description }}
  </li>
{% endfor %}
</ul>

This is not a complete list of components. They are being updated on a regular basis.
