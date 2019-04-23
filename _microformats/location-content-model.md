---
---
# Location content model

Both [adr] and [geo] use the [hCard XMDP profile]. See [Contact](contact-content-model.md) content model for details.

## [h-adr] [adr] combined microformat

**Root class:** h-adr adr

**Properties:**

**Note:** There is no "p-name" property in [h-adr]. If your address has an explicit name, it's likely a venue, and you should use [h-card] instead.

<dl>

<dt>p-street-address street-address</dt>
<dd>house/apartment number, floor, street name</dd>

<dt>p-extended-address extended-address</dt>
<dd>additional street details</dd>

<dt>p-post-office-box post-office-box</dt>
<dd>post office mailbox</dd>

<dt>p-locality locality</dt>
<dd>city/town/village</dd>

<dt>p-region region</dt>
<dd>state/county/province</dd>

<dt>p-postal-code postal-code</dt>
<dd>postal code, e.g. ZIP in the US</dd>

<dt>p-country-name country-name</dt>
<dd>should be full name of country, country code ok</dd>

<dt>p-label label</dt>
<dd>a mailing label, plain text, perhaps with preformatting</dd>

<dt>p-geo geo</dt>
<dd>

(or u-geo with a [RFC-5870] geo: URL), optionally embedded [h-geo]</dd>

<dt>p-latitude latitude</dt>
<dd>decimal latitude</dd>

<dt>p-longitude longitude</dt>
<dd>decimal longitude</dd>

<dt>p-altitude</dt>
<dd>

decimal altitude - new in vCard4 ([RFC-6350])</dd>
</dl>

## [h-geo] [geo] combined microformat

**Root class:** h-geo geo

**Properties:**
<dl>
<dt>p-latitude latitude</dt>
<dt>p-longitude longitude</dt>
<dt>p-altitude</dt>
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

[Rel-Tag]: http://microformats.org/wiki/rel-tag "rel=\"tag\" subject-identifier links"

[rfc-2119]: http://microformats.org/wiki/rfc-2119 "Requirement Levels keyword styles"

[citation]: http://microformats.org/wiki/citation "Citation microformat efforts"

[HTML 4]: http://www.w3.org/TR/REC-html40/ "W3C HTML 4.0 spec"

[XHTML]: http://www.w3.org/TR/xhtml1/ "W3C XHTML 1.0 spec"

[XMDP]: http://gmpg.org/xmdp/ "XML MetaData Profiles spec"
[hResume XMDP profile]: http://microformats.org/profile/hresume
[hCard XMDP profile]: http://microformats.org/profile/hcard

[XFN 1.1]: http://gmpg.org/xfn/11 "XHTML Friends Network spec"

[RFC-2445]: http://www.ietf.org/rfc/rfc2445 "iCalendar standard"

[RFC-6350]: http://tools.ietf.org/html/rfc6350 "vCard Format Spec"

[RFC-4770]: https://tools.ietf.org/rfc/rfc4770 "vCard IM Extensions"

[RFC-5870]: https://tools.ietf.org/html/rfc5870 "'geo' URI"