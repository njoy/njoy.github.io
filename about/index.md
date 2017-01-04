---
layout: page
title: About
permalink: /about/
---

NJOY is a nuclear data processing code developed at 
[Los Alamos National Laboratory](http://www.lanl.gov). 

## NJOY21—NJOY for the 21st Century
NJOY21 is the next generation of NJOY designed to modernize nuclear data processing including the ability to process nuclear data from multiple data formats. 

The goals for NJOY21 can be found at the [Vision, Mission, Goals](/about/NJOY21-Goals.html) page.

## NJOY2012
NJOY2012 is the current version of NJOY. It can be obtained from the [Feynman Center](http://www.lanl.gov/projects/feynman-center/index.php) at Los Alamos National Laboratory. The homepage for NJOY2012 can be found [here](http://t2.lanl.gov/nis/codes/NJOY12).

## Authors
NJOY is developed by the following individuals:

<ul>
{% for member in site.data.members %}
  <li>
    {{ member.name }}
      (<a href="https://github.com/{{ member.github }}">@{{ member.github }}</a>)
    {{ member.institution }}
  </li>
{% endfor %}
</ul>

## Collaborators
NJOY has benefited greatly from contributions from collaborators from around the 
world. The following list is just some of those who have contributed. If someone 
should be added to this list, please [contact us](mailto:njoy@lanl.gov).

<ul>
{% for collaborator in site.data.collaborators %}
  <li>
    {{ collaborator.name }}
    {% if collaborator.github %}
      (<a href="https://github.com/{{ collaborator.github }}">@{{ collaborator.github }}</a>)
    {% endif %}
    {{ collaborator.institution }}
  </li>
{% endfor %}
</ul>
