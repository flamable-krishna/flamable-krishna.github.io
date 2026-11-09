---
layout: default
title: Projects
permalink: /projects/
---
# Projects

I&rsquo;m learning and adding projects to my GitHub. This page showcases curated work &mdash; I&rsquo;ll update it as I release new projects.

<p><a href="https://github.com/flamble-gokul" target="_blank" rel="noopener noreferrer">View my GitHub profile &rarr;</a></p>

{% if site.data.projects and site.data.projects.size > 0 %}
<ul class="card-list">
  {% for project in site.data.projects %}
  <li class="card">
    <h3>{{ project.name }}</h3>
    {% if project.description %}<p>{{ project.description }}</p>{% endif %}
    <div class="links">
      {% if project.github %}<a href="{{ project.github }}" target="_blank" rel="noopener noreferrer">GitHub</a>{% endif %}
      {% if project.demo %}<a href="{{ project.demo }}" target="_blank" rel="noopener noreferrer">Live demo</a>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% else %}
<div class="notice">
  <strong>Coming soon.</strong> I haven&rsquo;t released projects yet &mdash; I&rsquo;ll add them here with GitHub links as I build and learn.
</div>
{% endif %}

## How I add projects

When I publish a project, I add it to <code>_data/projects.yml</code> with a name, description, and GitHub (and optional demo) link.
