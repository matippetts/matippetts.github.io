---
---
# Overview of microformats2 content model

The content model is based on microformats v2. The spec advises using both v2 [h-resume] and v1 [hResume] class-names. So I've combined them in the following presentations:

- [Resume]({% link _microformats/resume-content-model.md %}) content model
- [Contact]({% link _microformats/event-content-model.md %}) content model
- [Location]({% link _microformats/location-content-model.md %}) content model
- [Event]({% link _microformats/event-content-model.md %}) content model

## Class diagram

{% if site.url contains 'localhost' %}
  {% include_relative content-model-uml.md %}
{% endif %}

[h-resume]: http://microformats.org/wiki/h-resume "h-resume v2 microformat"
[hResume]: http://microformats.org/wiki/hResume "hResume v1 microformat"
