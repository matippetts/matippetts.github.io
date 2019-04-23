---
---
# Contact content model <!-- omit in toc -->

See also:
- [Location](location-content-model.md) content model

## [h-card] & [hCard]  combined microformats

Root class: h-card hcard

Properties:
<dl>
<dt>p-name fn</dt>
<dd>The full/formatted name of the person or organisation</dd>

<dt>n</dt>
<dd>

(v1 only) structured name, container for:
  <dl>

    <dt>p-honorific-prefix honorific-prefix</dt>
    <dd>e.g. Mrs., Mr. or Dr.</dd>

    <dt>p-given-name given-name</dt>
    <dd>given (often first) name</dd>

    <dt>p-additional-name additional-name</dt>
    <dd>other/middle name</dd>

    <dt>p-family-name family-name</dt>
    <dd>family (often last) name</dd>

    <dt>p-honorific-suffix</dt>
    <dd>e.g. Ph.D, Esq.</dd>

  </dl>
</dd>

<dt>p-nickname nickname</dt>
<dd>nickname/alias/handle - e.g. IRC nick</dd>

<dt>u-photo photo</dt>

<dt>dt-bday bday</dt>
<dd>birth date</dd>

<dt>p-adr adr</dt>
<dd>postal address

optionally embed an [h-adr]:
  <dl>

    <dt>p-post-office-box post-office-box</dt>

    <dt>p-extended-address extended-address</dt>
    <dd>apartment/suite/room name/number if any</dd>

    <dt>p-street-address street-address</dt>
    <dd>street number + name</dd>

    <dt>p-locality locality</dt>
    <dd>city/town/village</dd>

    <dt>p-region region</dt>
    <dd>state/county/province</dd>

    <dt>p-postal-code postal-code</dt>
    <dd>postal code, e.g. US ZIP</dd>

    <dt>p-country-name country-name</dt>
    <dd>country name</dd>

    <dt>type</dt>
    <dd>(v1 only)
    
    - work
    - home
    - pref (preferred)
    - postal
    - parcel
    - dom (domestic)
    - intl (international)
    </dd>

    <dt>value</dt>
    <dd>(v1 only)</dd>
  </dl>
</dd>

<dt>p-label label</dt>
<dd>formatted delivery address<br>
label : adr :: fn : n</dd>

<dt>p-tel tel</dt>
<dd>telephone number<br>
types:

- voice
- fax
- modem
- pager
- msg
- home
- work
- car
- cell
- video
- isdn
- pcs
- bbs

</dd>

<dt>u-email email</dt>
<dd>email address</dd>

<dt>mailer</dt>
<dd>(v1 only)<br>
email client</dd>

<dt>p-tz tz</dt>
<dd>timezone offset</dd>

<dt>(p-geo | u-geo) geo</dt>
<dd>

optionally embed an [h-geo]  
(i.e. `class="p-geo h-geo geo"` or `class="u-geo h-geo geo"`):
  <dl>
  
    <dt>p-latitude latitude</dt>
    <dd>decimal latitude</dd>

    <dt>p-longitude longitude</dt>
    <dd>decimal longitude</dd>

    <dt>p-altitude</dt>
    <dd>decimal altitude</dd>
  </dl>
</dd>

<dt>p-job-title title</dt>
<dd>job title, previously 'title' in [hCard], disambiguated</dd>

<dt>p-role role</dt>
<dd>description of role; contrast p-job-title</dd>

<dt>u-logo logo</dt>
<dd>a logo representing the person or organisation</dd>

<dt>agent</dt>
<dd>(v1 only)

(text | url | hCard)</dd>

<dt>p-org org</dt>
<dd>affiliated organization, optionally embed an [h-card]</dd>

<dt>p-organization-name organization-name</dt>
<dt>p-organization-unit organization-unit</dt>

<dt>p-category category</dt>
<dd>category/tag (kind of vCard)</dd>

<dt>p-note note</dt>
<dd>additional notes</dd>

<dt>dt-rev rev</dt>
<dd>last modification datetime</dd>

<dt>p-sort-string sort-string</dt>
<dd>string to sort by</dd>

<dt>u-sound</dt>
<dd>

sound file containing the proper pronunciation of the name property, per vCard ([RFC-6350])
</dd>

<dt>u-uid uid</dt>
<dd>universally unique identifier, typically canonical URL</dd>

<dt>u-url url</dt>
<dd>home page</dd>

<dt>class</dt>
<dd>(v1 only)</dd>

<dt>u-key key</dt>
<dd>cryptographic public key e.g. SSH or GPG</dd>

<dt>value</dt>
<dd>(v1 only)

See the [value-class-pattern] for details.</dd>

<dt>value-title</dt>
<dd>(v1 only)

See the [value-class-pattern value-title description] for details.</dd>

<dt>u-impp</dt>
<dd>

IM handle, per [RFC-4770], new in vCard4 ([RFC-6350])
</dd>

<dt>p-sex</dt>
<dd>

biological sex, new in vCard4 ([RFC-6350])  
("" | "M" | "F" | "O" | "N" | "U")
</dd>

<dt>p-gender-identity</dt>
<dd>

gender identity, new in vCard4 ([RFC-6350])  
freeform text
</dd>

<dt>dt-anniversary</dt>

</dl>

## XMDP profile

There is an [hCard XMDP profile]. It defines the following terms:
<dl>
  <dt id="vcard">vcard</dt>
  <dd>A container for the rest of the class names defined in this XMDP profile.  
  See section 1. of RFC 2426.
  </dd>

  <dt id="fn">fn</dt>
  <dd>See section 3.1.1 of RFC 2426.</dd>

  <dt id="n">n</dt>
  <dd>See section 3.1.2 of RFC 2426. May be inferred per Implied "N" Optimization.</dd>

  <dt id="family-name">family-name</dt>
  <dd>See "Family Name" in section 3.1.2 of RFC 2426.</dd>

  <dt id="given-name">given-name</dt>
  <dd>See "Given Name" in section 3.1.2 of RFC 2426.</dd>

  <dt id="additional-name">additional-name</dt>
  <dd>See "Additional Names" in section 3.1.2 of RFC 2426.</dd>

  <dt id="honorific-prefix">honorific-prefix</dt>
  <dd>See "Honorific Prefixes" in section 3.1.2 of RFC 2426.</dd>

  <dt id="honorific-suffix">honorific-suffix</dt>
  <dd>See "Honorific Suffixes" in section 3.1.2 of RFC 2426.</dd>
   
  <dt id="nickname">nickname</dt>
  <dd>See section 3.1.3 of RFC 2426.</dd>

  <dt id="photo">photo</dt>
  <dd>See section 3.1.4 of RFC 2426.<br>
  Typically used with an &lt;img&gt; tag.<br>
  Use the 'src' attribute for URI values.<br>
  Use the 'data:' URI scheme for binary values.</dd>

  <dt id="bday">bday</dt>
  <dd>See section 3.1.5 of RFC 2426.<br>
  Typically used with an &lt;abbr&gt; tag with the 'title' attribute for the date value, and a human readable date inside the element.</dd>
 
  <dt id="adr">adr</dt>
  <dd>See section 3.2.1 of RFC 2426.</dd>

  <dt id="post-office-box">post-office-box</dt>
  <dd>See "post office box" in section 3.2.1 of RFC 2426.</dd>

  <dt id="extended-address">extended-address</dt>
  <dd>See "extended address" in section 3.2.1 of RFC 2426.</dd>

  <dt id="street-address">street-address</dt>
  <dd>See "street address" in section 3.2.1 of RFC 2426.</dd>

  <dt id="locality">locality</dt>
  <dd>See "locality" in section 3.2.1 of RFC 2426.</dd>

  <dt id="region">region</dt>
  <dd>See "region" in section 3.2.1 of RFC 2426.</dd>

  <dt id="postal-code">postal-code</dt>
  <dd>See "postal code" in section 3.2.1 of RFC 2426.</dd>

  <dt id="country-name">country-name</dt>
  <dd>See "country name" in section 3.2.1 of RFC 2426.</dd>

  <dt id="type">type</dt>
  <dd>See "type" in the various sections of RFC 2426.</dd>

  <dt id="label">label</dt>
  <dd>See section 3.2.2 of RFC 2426.</dd>

  <dt id="tel">tel</dt>
  <dd>See section 3.3.1 of RFC 2426.</dd>

  <dt id="email">email</dt>
  <dd>See section 3.3.2 of RFC 2426.</dd>

  <dt id="mailer">mailer</dt>
  <dd>See section 3.3.3 of RFC 2426.</dd>

  <dt id="tz">tz</dt>
  <dd>See section 3.4.1 of RFC 2426.<br>
  Typically used with an &lt;abbr&gt; tag with the 'title' attribute for the tz value, and a human readable time zone inside the element.</dd>

  <dt id="geo">geo</dt>
  <dd>See section 3.4.2 of RFC 2426.</dd>

  <dt id="latitude">latitude</dt>
  <dd>See "latitude" in section 3.4.2 of RFC 2426.</dd>

  <dt id="longitude">longitude</dt>
  <dd>See "longitude" in section 3.4.2 of RFC 2426.</dd>

   <dt id="title">title</dt>
  <dd>See section 3.5.1 of RFC 2426.</dd>

  <dt id="role">role</dt>
  <dd>See section 3.5.2 of RFC 2426.</dd>

  <dt id="logo">logo</dt>
  <dd>See section 3.5.3 of RFC 2426.<br>
  Typically used with an &lt;img&gt; tag.<br>
  Use the 'src' attribute for URI values. Use the 'data:' URI scheme for binary values.</dd>

  <dt id="agent">agent</dt>
  <dd>See section 3.5.4 of RFC 2426.<br>
  If the value is a vCard, then use a nest hCard. For simplicity in that case, the same element that has the class name of "agent" should use the class name of "vcard".</dd>

  <dt id="org">org</dt>
  <dd>See section 3.5.5 of RFC 2426.</dd>

  <dt id="organization-name">organization-name</dt>
  <dd>See "Organization Name" in section 3.5.5 of RFC 2426.<br>
  May be inferred per Implied "organization-name" Optimization.</dd>

  <dt id="organization-unit">organization-unit</dt>
  <dd>See "Organization Unit" in section 3.5.5 of RFC 2426.</dd>    

  <dt id="category">category</dt>
  <dd>See section 3.6.1 of RFC 2426.</dd>

  <dt id="note">note</dt>
  <dd>See section 3.6.2 of RFC 2426.</dd>

  <dt id="rev">rev</dt>
  <dd>See section 3.6.4 of RFC 2426.<br>
  Typically used with an &lt;abbr&gt; tag with the 'title' attribute for the date value, and a human readable date inside the element.</dd>

  <dt id="sort-string">sort-string</dt>
  <dd>See section 3.6.5 of RFC 2426.</dd>

  <dt id="sound">sound</dt>
  <dd>See section 3.6.6 of RFC 2426.<br>
  Typically used with either an &lt;a&gt; or &lt;object&gt; tag. Use the 'data:' URI scheme for binary values.</dd>

  <dt id="uid">uid</dt>
  <dd>See section 3.6.7 of RFC 2426.</dd>

  <dt id="url">url</dt>
  <dd>See section 3.6.8 of RFC 2426. Typically used with an &lt;a&gt; tag.</dd>

  <dt id="class">class</dt>
  <dd>See section 3.7.1 of RFC 2426.</dd>

  <dt id="key">key</dt>
  <dd>See section 3.7.2 of RFC 2426.<br>
  Typically used with an &lt;abbr&gt; tag with the 'title' attribute for the key value, and a human readable key equivalent inside the element.</dd>
     
  <dt id="value">value</dt>
  <dd>This class name is used to distinguish the <em>actual</em> value of a property from any other cruft that may be in the containing element representing the property.<br>
  See the <a href="http://microformats.org/wiki/value-class-pattern">value-class-pattern</a> for details.</dd>

  <dt id="value-title">value-title</dt>
  <dd>This class name is used to distinguish the <em>actual</em> value of a property, specifically in the 'title' attribute of the element, from the element contents and the element representing the containing property.<br>
  See the <a href="http://microformats.org/wiki/value-class-pattern#Parsing_value_from_a_title_attribute">value-class-pattern value-title description</a> for details.</dd>

</dl>

[h-resume]: http://microformats.org/wiki/h-resume "h-resume v2 microformat"
[hResume]: http://microformats.org/wiki/hResume "hResume v1 microformat"

[h-card]: http://microformats.org/wiki/h-card "h-card v2 microformat"
[hCard]: http://microformats.org/wiki/hcard "hCard v1 microformat"

[h-adr]: http://microformats.org/wiki/h-adr "h-adr v2 microformat"
[adr]: http://microformats.org/wiki/adr "adr v1 microformat"

[h-geo]: http://microformats.org/wiki/h-geo "h-geo v2 microformat"
[geo]: http://microformats.org/wiki/geo "geo v1 microformat"

[tel]: http://microformats.org/wiki/phone_number "telephone number v1 microformat"

[h-event]: http://microformats.org/wiki/h-event "h-event v2 microformat"
[hCalendar]: http://microformats.org/wiki/hcalendar "hCalendar v1 microformat"

[include pattern]: http://microformats.org/wiki/include-pattern "include file pattern"

[value-class-pattern]: http://microformats.org/wiki/value-class-pattern

[value-class-pattern value-title details]: http://microformats.org/wiki/value-class-pattern#Parsing_value_from_a_title_attribute

[Rel-Tag]: http://microformats.org/wiki/rel-tag "rel=\"tag\" subject-identifier links"

[rfc-2119]: http://microformats.org/wiki/rfc-2119 "Requirement Levels keyword styles"

[citation]: http://microformats.org/wiki/citation "Citation microformat efforts"

[HTML 4]: http://www.w3.org/TR/REC-html40/ "W3C HTML 4.0 spec"

[XHTML]: http://www.w3.org/TR/xhtml1/ "W3C XHTML 1.0 spec"

[XMDP]: http://gmpg.org/xmdp/ "XML MetaData Profiles spec"
[hResume XMDP profile]: http://microformats.org/profile/hresume
[hCard XMDP profile]: http://microformats.org/profile/hcard

[XFN 1.1]: http://gmpg.org/xfn/11 "XHTML Friends Network spec"

[RFC-2445]: http://www.ietf.org/rfc/rfc2445.txt "iCalendar standard"

[RFC-6350]: http://tools.ietf.org/html/rfc6350 "vCard Format Spec"

[RFC-4770]: https://tools.ietf.org/rfc/rfc4770 "vCard IM Extensions"

[RFC-5870]: https://tools.ietf.org/rfc/rfc5870 "'geo' URI"