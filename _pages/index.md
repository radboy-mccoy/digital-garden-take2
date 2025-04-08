---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

Here lives my assorted creative output. I hope you'll enjoy looking around and keep coming back as the site grows. 

<img src="{{ site.baseurl }}/assets/welcome.jpeg"/>

<strong>Recently Updated</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
