---
title: Portfolio Projects
author: Mark Tippetts
published: true
---
Public (on GitHub):
{% assign public_projects = site.projects | where:"visibility","public" %}
{% for project in public_projects %}
- [{{ project.title }}]({{ project.url }}) {{ project.location }}
{% endfor %}

Private (on BitBucket):
{% assign private_projects = site.projects | where:"visibility","private" %}
{% for project in private_projects %}
- [{{ project.title }}]({{ project.url }}){{ project.location }}
{% endfor %}

Ideas:
{% for idea in site.ideas  %}
- {{ idea.title }}
{% endfor %}
- Recipes (Netlify CMS)
- Fitness tracker
- Personal accounting software
- Epsilon Visual Design Tools
- Firewall visualization
- Pandora desktop client
- Pandora export to Spotify
