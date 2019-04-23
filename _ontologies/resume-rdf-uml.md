---
---
{% if site.url contains 'localhost' %}
{% plantuml %}
```plantuml
@startuml
skinparam ArrowFontColor MediumBlue
package cv {
  class CV {
    lastUpdate
    cvTitle
    cvDescription
    cvCopyright
    cvIsConfidential
    cvIsActive
  }
  CV -> Person: aboutPerson
  CV *-- WorkHistory: hasWorkHistory
  CV *-- Education: hasEducation
  CV *-- Course: hasCourse
  CV *-- Skill: hasSkill
  CV *-- Reference: hasReference
  CV *-- Target: hasTarget
  CV *-- OtherInfo: hasOtherInfo
  hide abstract class CV_Entry
  hide CV_Entry --|> rdfs.Resource
  hide CV_Entry <|-- WorkHistory
  hide CV_Entry <|-- Education
  hide CV_Entry <|-- Course
  hide CV_Entry <|-- Skill
  hide CV_Entry <|-- Reference
  hide CV_Entry <|-- Target
  hide CV_Entry <|-- OtherInfo
  together {
    class Course {
      courseDescription
      courseFinishDate
      courseStartDate
      courseTitle
      courseURL
      isCertification
    }
    Course -- Organization: organizedBy
    class Education {
      degreeType
      eduDescription
      eduGradDate
      eduMajor
      eduMinor
      eduStartDate
    }
    Education -- EducationalOrg: studiedIn
    class WorkHistory {
      CVCareerLevel careerLevel
      startDate
      endDate
      isCurrent
      jobDescription
      jobTitle
      CVJobType jobType
      numSubordinates
    }
    WorkHistory -- Company: employedIn
  }
  together {
    class Company {
      Industry
    }
    Company --|> Organization
    class EducationalOrg
    EducationalOrg --|> Organization
    abstract class Organization {
      Locality
      Name
      Notes
      URL
    }
    Organization --|> rdfs.Resource
    Organization -- NSO.Country: Country
  }
  together {
    class Person {
      SexProperty gender
      birthPlace
      hasNationality
      hasCitizenship
      MaritalStatus familyStatus
      noOfChildren
      hasDriversLicense
    }
    abstract class Reference
    Reference -- Person: referenceBy
    Reference <|-- PersonalReference
    Reference <|-- ProfessionalReference
    class OtherInfo {
      OtherCVInfoType otherInfoType
      otherInfoDescription
    }
  }
  together {
    class Skill {
      skillName
      skillLevel
      skillLastUsed
      skillYearsOfExperience
    }
    class LanguageSkill {
      lngSkillLevelReading
      lngSkillLevelWritten
    }
    Skill <|-- LanguageSkill
    class Target {
      targetCareerLevel
      targetCompanyDescription
      targetCompanyIndustry
      targetCompanySize
      targetJobDescription
      CVJobMode targetJobMode
      CVJobType targetJobType
      targetSalery
      targetSaleryCurrency
      weeksNoticePeriod
      conditionWillRelocate
      conditionWillTravel
    }
    Target -- NSO.Country: targetCountry
  }
}
namespace NSO {
  class Country {
    code
    name
  }
}

@enduml
```
{% endplantuml %}
{% endif %}
