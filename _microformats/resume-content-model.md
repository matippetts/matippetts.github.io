---
---
# Resume content model <!-- omit in toc -->

See also:
- [Event](event-content-model.md) content model
- [Contact](contact-content-model.md) content model
- [Location](location-content-model.md) content model

There is an [hResume XMDP profile].

## [h-resume] & [hResume] combined microformats

**Root class:** `h-resume hresume`

**Properties:**
<dl>
<dt>p-name</dt>
<dd>brief name of the resume</dd>

<dt>p-summary summary</dt>  
<dd>overview of qualifications and objectives</dd>

<dt>p-contact contact</dt>
<dd>

- v2: current contact info in an [h-card]
- v1: must use [hCard]; should use \<address> + [hCard].

</dd>

<dt>p-education education</dt>
<dd>

- v2: an education [h-event] event, years, embedded [h-card] of the school, location.  
- v1: One or more [hcalendar] events with the class name 'education', with an embedded [hCard] indicating the name of school, address of school etc.

</dd>

<dt>p-experience experience</dt>
<dd>

- v2: a job or other professional experience [h-event] event, years, embedded [h-card] of the organization, location, job-title.  
- v1: One or more [hcalendar] events with the class name 'experience', with an embedded [hCard] indicating the job title, name of company, address of company etc.

</dd>

<dt>p-skill skill</dt>
<dd>

- v2: a skill or ability, optionally including level and/or duration of experience
- v1: phrases or keywords using the [rel-tag] microformat with the class name `skill`.

</dd>

<dt>p-affiliation affiliation</dt>
<dd>

- v2: an affiliation with an [h-card] organization
- v1: the class name `affiliation` along with an [hcard] of the organization

</dd>

<dt>publications</dt>
<dd>

One or more citations. Use \<cite> tag.  
When there is a [citation] microformat, then that can be used in combination with the cite element to further markup the components of the citation.

</dd>
</dl>

[h-resume]: http://microformats.org/wiki/h-resume "h-resume v2 microformat"
[hResume]: http://microformats.org/wiki/hResume "hResume v1 microformat"

[h-card]: http://microformats.org/wiki/h-card "h-card v2 microformat"
[hCard]: http://microformats.org/wiki/hcard "hCard v1 microformat"

[h-event]: http://microformats.org/wiki/h-event "h-event v2 microformat"
[hCalendar]: http://microformats.org/wiki/hcalendar "hCalendar v1 microformat"

[rel-tag]: http://microformats.org/wiki/rel-tag "rel=\"tag\" subject-identifier links"

[citation]: http://microformats.org/wiki/citation "Citation microformat efforts"

[XMDP]: http://gmpg.org/xmdp/ "XML MetaData Profiles spec"
[hResume XMDP profile]: http://microformats.org/profile/hresume
[hCard XMDP profile]: http://microformats.org/profile/hcard
