# Mark Tippetts - Developer Portfolio <!-- omit in toc -->

Content model:

## [hResume] microformat

Properties:

<dl>
<dt>summary (optional)</dt>  
<dd>

text.
</dd>

<dt>contact info (required)</dt>
<dd>

must use [hCard];  
should use \<address> + [hCard].
</dd>

<dt>experience (optional)</dt>
<dd>

One or more [hcalendar] events with the class name 'experience', with an embedded [hCard] indicating the job title, name of company, address of company etc.
</dd>

<dt>education (optional)</dt>
<dd>

One or more [hcalendar] events with the class name 'education', with an embedded [hCard] indicating the name of school, address of school etc.
</dd>

<dt>skills (optional)</dt>
<dd>

phrases or keywords using the [rel-tag] microformat with the class name 'skill'.
</dd>

<dt>affiliations</dt>
<dd>

the class name affiliation along with an [hcard] of the organization
</dd>

<dt>publications</dt>
<dd>

One or more citations. Use cite tag.

When there is a [citation] microformat, then that can be used in combination with the cite element to further markup the components of the citation.
</dt>
</dl>

## [hCard] microformat

Properties:
<dl>
</dl>

## [hCalendar] microformat

Properties:
<dl>
</dl>

[hResume]: http://microformats.org/wiki/hResume "hResume microformat"

[hCard]: http://microformats.org/wiki/hcard "hCard microformat"

[hCalendar]: http://microformats.org/wiki/hcalendar "hCalendar microformat"

[include pattern]: http://microformats.org/wiki/include-pattern "include file pattern"

[Rel-Tag]: http://microformats.org/wiki/rel-tag "rel=\"tag\" subject-identifier links"

[rfc-2119]: http://microformats.org/wiki/rfc-2119 "Requirement Levels keyword styles"

[citation]: http://microformats.org/wiki/citation "Citation microformat efforts"

[HTML 4]: http://www.w3.org/TR/REC-html40/ "W3C HTML 4.0 spec"

[XHTML]: http://www.w3.org/TR/xhtml1/ "W3C XHTML 1.0 spec"

[XMDP]: http://gmpg.org/xmdp/ "XML MetaData Profiles spec"

[XFN 1.1]: http://gmpg.org/xfn/11 "XHTML Friends Network spec"

[RFC2445]: http://www.ietf.org/rfc/rfc2445.txt "iCalendar standard"