---
---
# Event content model <!-- omit in toc -->

[hCalendar] is an incomplete mapping of the [RFC-2445] iCalendar standard. Only `dtstart` and `summary` are required. The list of optional properties is incomplete.

See also:
- [Contact](contact-content-model.md) content model
- [Location](location-content-model.md) content model

## [h-event] & [hCalendar] combined microformat

**Root class:** `h-event vevent`

**Properties:**
<dl>
<dt>p-name summary</dt>
<dd>event name (or title)</dd>

<dt>p-summary</dt>
<dd>short summary of the event</dd>

<dt>dt-start dtstart</dt>
<dd>datetime the event starts</dd>

<dt>dt-end dtend</dt>
<dd>datetime the event ends</dd>

<dt>dt-duration duration</dt>
<dd>duration of the event</dd>

<dt>p-description description</dt>
<dd>more detailed description of the event</dd>

<dt>u-url url</dt>
<dd>permalink for the event</dd>

<dt>p-category category</dt>
<dd>event category(ies)/tag(s)<br>
e.g.: MEETING, APPOINTMENT, CONFERENCE. EXPO</dd>

<dt>p-location location</dt>
<dd>where the event takes place,

optionally embedded [h-card], [h-adr], or [h-geo]
</dd>

<dt>p-attendee attdendee</dt>
<dd>

- v2: a person attending the event, optionally embed [h-card]
- v1: attdendee (partstat, role)
  - partstat: NEEDS-ACTION, ACCEPTED, DECLINED, TENTATIVE, DELEGATED
  - role: REQUIRED, OPTIONAL, NON-PARTICIPANT, x-name
  
</dd>

<dt>contact</dt>
<dd>(v1 only)</dd>

<dt>organizer</dt>
<dd>(v1 only)</dd>

<dt>attach</dt>
<dd>(v1 only)<br>
Alternative content models:

1. `<img src="..." alt="">`
2. `<object data="...">alt text</object>`
3. `<a class="attach" href="...">alt text</a>`

</dd>

<dt>status</dt>
<dd>v1 only</dd>

</dl>

## XMDP profile

There is an [hCalendar XMDP profile]. It defines the following terms:
<dl>
  <dt id="vcalendar">vcalendar</dt>
  <dd>
  A container for one or more events (vevent).<br>
  This property is optional; if there is only one event then omit it.<br>
  See section 1. of RFC 2445.
  </dd>

  <dt id="vevent">vevent</dt>
  <dd>
  A container for one event.<br>
  See section 4.6.1 of RFC 2445.
  </dd>

  <dt id="dtstart">dtstart</dt>
  <dd>
  Date/time of the start of the event.<br>
  See section 4.8.2.4 of RFC 2445.
  </dd>

  <dt id="dtend">dtend</dt>
  <dd>
  Date/time of the end of the event.<br>
  See section 4.8.2.2 of RFC 2445.
  </dd>

  <dt id="duration">duration</dt>
  <dd>
  Length of the event.<br>
  See section 4.8.2.5 of RFC 2445.
  </dd>

  <dt id="summary">summary</dt>
  <dd>
  Short synopsis, title, or  name of the event.<br>
  See section 4.8.1.12 of RFC 2445.
  </dd>

  <dt id="uid">uid</dt>
  <dd>
  A globally unique identifier for the event; typically a URL is used.<br>
  See section 4.8.4.7 of RFC 2445.
  </dd>

  <dt id="dtstamp">dtstamp</dt>
  <dd>
  Date/time of when the document containing information about the event was created.<br>
  See section 4.8.7.2 of RFC 2445.
  </dd>

  <dt id="method">method</dt>
  <dd>
  Function of the event object.<br>
  Values for this property are: PUBLISH, REQUEST, REPLY, ADD, CANCEL, REFRESH, COUNTER, or DECLINECOUNTER.<br>
  For example, a value of REQUEST indicates that a request is being made for the event to occur.<br>
  See section 4.7.2 of RFC 2445.
  </dd>

  <dt id="category">category</dt>
  <dd>
  Category of the event object.<br>
  Note: this property may be repeated (an event may belong in several categories).<br>
  Common values are: MEETING, APPOINTMENT, CONFERENCE, EXPO.<br>
  See section 4.8.1.2 of RFC 2445.
  </dd>

  <dt id="location">location</dt>
  <dd>
  Tells where the event is to be held.<br>
  May be represented by nested <a href="http://microformats.org/wiki/hcard">hCard record</a>, <a href="http://microformats.org/wiki/adr">adr record</a>, <a href="http://microformats.org/wiki/geo">geo record</a>, or combination thereof.<br>
  See sections 4.8.1.7 and 4.8.1.6 of RFC 2445.
  </dd>

  <dt id="url">url</dt>
  <dd>
  A URL to a page that contains the definitive/preferred information about an event;<br>
  UID and URL are typically the same.<br>
  See section 4.8.4.6 of RFC 2445, except "url" may occur more than once in an hCalendar event.
  </dd>

  <dt id="description">description</dt>
  <dd>
  A more detailed synopsis of the event than that provided by summary.<br>
  See section 4.8.1.5 of RFC 2445.
  </dd>

  <dt id="last-modified">last-modified</dt>
  <dd>
  Date/time the information about the event was updated.<br>
  See section 4.8.7.3 of RFC 2445.
  </dd>

  <dt id="status">status</dt>
  <dd>
  Status of the calendar event.<br>
  Values are: TENTATIVE, CONFIRMED, CANCELLED.<br>
  See section 4.8.1.11 of RFC 2445.
  </dd>

  <dt id="class">class</dt>
  <dd>
  Access classification of the event information;<br>
  Values are: PUBLIC, PRIVATE, CONFIDENTIAL.<br>
  See section 4.8.1.3 of RFC 2445.
  </dd>

  <dt id="attendee">attendee</dt>
  <dd>
  An individual invited to attend the event;<br>
  An event container may contain more than one attendee record;<br>
  May be represented by nested <a href="http://microformats.org/wiki/hcard">hCard record</a>.<br>
  See section 4.8.4.1 of RFC 2445.
  </dd>
   
  <dt id="partstat">partstat</dt>
  <dd>
  The participation-status of an individual invited to attend the event;<br>
  Subproperty of "attendee";<br>
  See section 4.2.12 of RFC 2445.
  </dd>
   
  <dt id="role">role</dt>
  <dd>
  The role of an individual invited to attend the event;<br>
  Subproperty of "attendee";<br>
  See section 4.2.16 of RFC 2445.
  </dd>

  <dt id="contact">contact</dt>
  <dd>
  Contact information associated with the event;<br>
  May be represented by nested <a href="http://microformats.org/wiki/hcard">hCard record</a>.<br>
  See section 4.8.4.2 of RFC 2445.
  </dd>

  <dt id="organizer">organizer</dt>
  <dd>
  The organizer associated with the event.<br>
  May be represented by nested <a href="http://microformats.org/wiki/hcard">hCard record</a>.<br>  
  See section 4.8.4.3 of RFC 2445.
  </dd>

  <dt id="attach">attach</dt>
  <dd>
  An attached resource associated with the event, such as a photo.<br>
  See section 4.8.1.1 of RFC 2445.
  </dd>

  <dt id="value">value</dt>
  <dd>
  This class name is used to distinguish the <em>actual</em> value of a property from any other cruft that may be in the containing element representing the property.<br>
  See the <a href="http://microformats.org/wiki/value-class-pattern"> value-class-pattern</a> for details.
  </dd>

  <dt id="value-title">value-title</dt>
  <dd>
  This class name is used to distinguish the <em>actual</em> value of a property, specifically in the 'title' attribute of the element, from the element contents and the element representing the containing property.<br>
  See the <a href="http://microformats.org/wiki/value-class-pattern#Parsing_value_from_a_title_attribute">value-class-pattern value-title description</a> for details.
  </dd>

</dl>

[h-event]: http://microformats.org/wiki/h-event "h-event v2 microformat"
[hCalendar]: http://microformats.org/wiki/hcalendar "hCalendar v1 microformat"

[h-card]: http://microformats.org/wiki/h-card "h-card v2 microformat"
[hCard]: http://microformats.org/wiki/hcard "hCard v1 microformat"

[h-adr]: http://microformats.org/wiki/h-adr "h-adr v2 microformat"
[adr]: http://microformats.org/wiki/adr "adr v1 microformat"

[h-geo]: http://microformats.org/wiki/h-geo "h-geo v2 microformat"
[geo]: http://microformats.org/wiki/geo "geo v1 microformat"

[tel]: http://microformats.org/wiki/phone_number "telephone number v1 microformat"

[include pattern]: http://microformats.org/wiki/include-pattern "include file pattern"

[Rel-Tag]: http://microformats.org/wiki/rel-tag "rel=\"tag\" subject-identifier links"

[rfc-2119]: http://microformats.org/wiki/rfc-2119 "Requirement Levels keyword styles"

[hCalendar XMDP profile]: http://microformats.org/profile/hcalendar
[hCard XMDP profile]: http://microformats.org/profile/hcard

[XFN 1.1]: http://gmpg.org/xfn/11 "XHTML Friends Network spec"

[RFC-2445]: http://www.ietf.org/rfc/rfc2445.txt "iCalendar spec"

[RFC-6350]: http://tools.ietf.org/html/rfc6350 "vCard Format spec"

[RFC-4770]: https://tools.ietf.org/rfc/rfc4770.txt "vCard IM Extensions spec"
