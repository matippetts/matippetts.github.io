---
---
# Structured Data for Resumes &mdash; Existing Work

## Summary

A decade ago, numerous efforts were underway to create vocabularies and ontologies related to CVs and resumes. Today, few have survived link-rot, and none have thrived.

In practice, most people use microdata with the Person schema, essentially producing a user profile rather than a resume or CV. One major drawback to this approach is that the results tend to biographical, rather than functional, descriptions. But (in principle, if [not in practice](http://web.archive.org/web/20111101093707/http://mkapor.posterous.com/beyond-arrington-and-cnn-lets-look-at-the-rea)) employers should be far more interested in your capabilities than in your personal narrative.

With the exception of the [microformats h-resume spec]({% link _microformats/content-model-overview.md %}), CV/Resume ontologies generally address this discrepancy with some sort of mapping of abilities to years of experience or skill level (or both). The Cognitive Characteristics Ontology attempts to model knowledge and abilities by representing competencies as weighted interests. It enables some interesting features, like tracking the development of competencies through time. But it suffers from a number of formal difficulties. JSON Resume takes a far simpler approach by defining "skill level" and "language fluency" properties. But it falls short of enumerating values for these properties, which severely limits their suitability for scoring and ranking resumes in datasets. RDFResume suggests using an integer value in the range 0-5, which approximates a Likert scale.

## Schemas

- [ResumeRDF ontology]({% link _ontologies/resume-rdf-ontology.md %})
- [JSON Resume]({% link _ontologies/json-resume.md %})
- [Cognitive Characteristics Ontology]({% link _ontologies/cognitive-characteristics-ontology.md %})
- ~~[Description Of A Career vocabulary](https://www.w3.org/wiki/DescriptionOfACareerVocabulary)~~

## Thread on [public-vocabs](https://lists.w3.org/Archives/Public/public-vocabs/) mailing list

- ["Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0003.html)
  - [Dan Brickley: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0004.html)
    - [Tantek Çelik: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0005.html)
      - [Dan Brickley: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0006.html)
        - [George Katsanos: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0011.html)
      - [Hugh Paterson III: "Re: [uf-discuss] Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0007.html)
    - [Bob Ferris: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0008.html)
      - [Bernard Vatant: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0009.html)
        - [Bob Ferris: "Re: Curriculum Vitae (resumé) schema"](https://lists.w3.org/Archives/Public/public-vocabs/2011Oct/0010.html)

## Software and CMS Plugins

- [Foafpress](http://foafpress.org/) - PHP web app (designed for Apache) that publishes FOAF Person and Group profiles supporting Linked Data
- [CurriculumVitae](https://asphaltthemes.com/curriculumvitae/) - WordPress theme

## Examples

### Example 1: [danielantelo/microdata_resume_cv.html](https://gist.github.com/danielantelo/218015d40f346b964aac) gist

Uses [microdata] format

Features:

- Personal details
- Skills
- Experience
- Education

Schemas:

- [Person]
- [ItemList]
- [Organization]
- [Place]
- [PostalAddress]
- Event/Job &mdash; see the (obsolete) ["slash-based" extension mechanism](https://www.schema.org/docs/old_extension.html)
- [EducationalOrganization](http://schema.org/EducationalOrganization)

See also: [Actual resume](http://danielantelo.github.io/personal-website/)

### Example 2: [HTML5 Schema.org CV Boilerplate](https://codepen.io/tarranjones/pen/Bpgqvj) Codepen

Uses [microdata] format

Schemas:

- [Person]
- [PostalAddress]
- [CollegeOrUniverity]
- [Event]
- [HighSchool]
- [Organization]
- [ItemList] for Skills

### Example 3: ["How to Create an HTML5 Microdata Powered Resume"](https://code.tutsplus.com/tutorials/how-to-create-an-html5-microdata-powered-resume--net-22046)

Uses [microdata] format and "Authorship Markup" (an obsolete spec using rel="me" and rel="author" links to Google+ profiles).

Schemas:

- [Person]
- [PostalAddress]
- [ItemList] for Skills
- [Organization] for Experience
- [Article] for Publications
- [EducationalOrganization] for Education

[Person]: http://schema.org/Person
[ItemList]: http://schema.org/ItemList
[Organization]: http://schema.org/Organization
[Place]: http://schema.org/Place
[PostalAddress]: http://schema.org/PostalAddress
[Event]: http://schema.org/Event/Job
[EducationalOrganization]: http://schema.org/EducationalOrganization
