---
---
# The Cognitive Characteristics Ontology

## Summary

The [Cognitive Characteristics Ontology](http://purl.org/ontology/cco/20100926/cognitivecharacteristics.html#) was developed in 2010 by Dan Brickley, better known for co-authoring [FOAF](http://xmlns.com/foaf/spec/) and running [Schema.org](https://schema.org/docs/about.html). The CCO describes a type hierarchy of *"cognitive patterns:"*

- interest - a topic of interest to an agent (equiv. to [foaf:topic_interest](http://xmlns.com/foaf/spec/#term_topic_interest))
- setting - a setting or preference with regards to an environment or application
- competence
  - skill - procedural memory
  - expertise - semantic memory
  - belief - "an uncertain relation"

The CCO uses activities to distinguish modes of engagement with a topic, using the example of *watching* football vs. *playing* the game. This aligns well with the difference between "expertise" and "skill."

The CCO also ascribes statistics to cognitive characteristics:

- overall weight - interest in a topic
- attention duration
  - longest duration - longest continuous span of engagement
  - ultimative duration - cumulative span of interest (including gaps)

These can be used as the "skill level" and "years experience" expected in resumes.

## UML

{% if site.url contains 'localhost' %}
    {% include_relative cco-uml.md %}
{% endif %}

## Context

The CCO has the following dependencies:

- [Weighting Ontology](http://smiy.sourceforge.net/wo/spec/weightingontology.html#)
- [Statistical Core Ontology (SCOVO)](http://vocab.deri.ie/scovo)
- [Event Ontology](http://motools.sourceforge.net/event/event.html)
- [OWL-Time](http://www.w3.org/2006/time#)
- [WGS80 Geo Positioning Ontology](http://www.w3.org/2003/01/geo/wgs84_pos#)
- [Association Ontology](http://smiy.sourceforge.net/ao/spec/associationontology.html#activity)
- [FOAF](http://xmlns.com/foaf/spec/)

SCOVO is deprecated by the [Data Cube Vocabulary](http://www.w3.org/TR/vocab-data-cube/).

## Classes

- CognitiveCharacteristic - Continuant concept
- CharacteristicDynamics - Occurrent concept to describe changes and periods

## Properties

- activity
- <a id="agent">agent</a> - inverse of [habit](#habit)
- <a id="habit">habit</a> - inverse of [agent](#agent)
- appear_time - when a cognitive pattern gets someone's attention
- attention_duration
  - ultimative_duration
  - longest_duration
- characteristic
- characteristic_dynamics
- cognitive_characteristic
  - interest
  - setting
  - competence
    - belief
    - skill
    - expertise
- evidence - basis for ascribing characteristics and dynamics
- not_interested_in
- overall_weight
- statistical_item
- topic

## Related Works

### Sources and Influences

See [announcement](https://smiy.wordpress.com/2010/10/19/the-cognitive-characteristics-ontology/) blog entry.

### Similar Efforts

Other vocabularies, ontologies, etc. for describing skills and interests
