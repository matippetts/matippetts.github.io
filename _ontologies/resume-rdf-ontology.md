---
---
# The ResumeRDF Ontology

[Formal Specfication](http://rdfs.org/resume-rdf/)

  - [Schema](http://rdfs.org/resume-rdf/cv.rdfs#)
  - [Enumerated lists](http://rdfs.org/resume-rdf/base.rdfs#)

## Related resources

- The specification is based on Uldis Bojars's thesis [*Modelling of Resume Data in the Semantic Web Using RDF*](http://captsolo.net/semweb/resume/Semantic_Web-Modelling_of_Resumes_with_RDF.pdf) (in Latvian)
- See also: [Extending FOAF with Resume Information](https://www.w3.org/2001/sw/Europe/events/foaf-galway/papers/pp/extending_foaf_with_resume/)
- Uldis Bojars's [collection of Semantic Web resources](http://captsolo.net/semweb/)
- Known for: [SIOC (Semantically Interlinked Online Communities) Project](http://sioc-project.org/)
  - [SIOC Core Ontology Specification](http://rdfs.org/sioc/spec/) (ed.)

## Context

- [ISO-3116 Countries](http://www.daml.org/2001/09/countries/countries.daml#)
- [RDFS mapping of WordNet](http://xmlns.com/2001/08/wordnet/)
  - [WordNet home](https://wordnet.princeton.edu/)

## UML
{% if site.url contains 'localhost' %}
  {% include_relative resume-rdf-uml.md %}
{% endif %}

## Classes

CV
CV_Entry
Company
Course
Education
EducationalOrg
LanguageSkill
Organization
OtherInfo
Person
PersonalReference
ProfessionalReference
Refernece
Skill
Target
WorkHistory

Properties: | Country | Industry | Locality | Name | Notes | URL | aboutPerson | birthPlace | careerLevel | conditionWillRelocate | conditionWillTravel | courseDescription | courseFinishDate | courseStartDate | courseTitle | courseURL | cvCopyright | cvDescription | cvIsActive | cvIsConfidential | cvTitle | degreeType | eduDescription | eduGradDate | eduMajor | eduMinor | eduStartDate | employedIn | endDate | gender | hasCitizenship | hasCourse | hasDriversLicense | hasEducation | hasNationality | hasOtherInfo | hasReference | hasSkill | hasTarget | hasWorkHistory | isCertification | isCurrent | jobDescription | jobTitle | jobType | lastUpdate | lngSkillLevelReading | lngSkillLevelWritten | maritalStatus | noOfChildren | numSubordinates | organizedBy | otherInfoDescription | otherInfoType | referenceBy | skillLastUsed | skillLevel | skillName | skillYearsExperience | startDate | studiedIn | targetCareerLevel | targetCompanyDescription | targetCompanyIndustry | targetCompanySize | targetCountry | targetJobDescription | targetJobMode | targetJobType | targetSalary | targetSalaryCurrency | weeksNoticePeriod |