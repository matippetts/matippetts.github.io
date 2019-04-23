---
---
# Structured Data

Structured data is a set of approaches to encoding machine-readable data in the markup of human-readable HTML documents. There are several standards for structured data, each with various degrees of adoption. These include:

- [JSON-LD](#json-ld)
- [RDFa](#rdfa)
- [microdata](#microdata)
- [microformat]()
- [microformats2](http://microformats.org/wiki/microformats2)

In addition, there is the [XMDP profile](#xmdp-profiles) standard, of special importance to microformats v1.

All of these are discussed briefly below.

## Adoption

### Consumers

#### Search engines

Google Search supports structured data in JSON-LD, RDFa, and microdata formats. A list of supported data-types is available from the [developers' reference overview](https://developers.google.com/search/reference/overview). (Expand "Structured data" in the left-hand-side nav-bar to view the list.) A subset of these data-types (called "Rich Snippets") may appear in rich results and other special search features (see [Qualifying content types](https://developers.google.com/search/docs/guides/mark-up-content#content_types)). There are also [guidelines](https://developers.google.com/search/docs/guides/mark-up-listings) for recipes, courses, and articles to appear in carousel listings. Google provides a [Structured Data Testing tool](https://search.google.com/structured-data/testing-tool) and [Rich result status reports](https://support.google.com/webmasters/answer/7552505) to help developers, as well as a [tutorial](https://codelabs.developers.google.com/codelabs/structured-data/index.html#0) on their use.

Bing also provides [guidance on using structured data](), if anybody cares. ;-)

#### Social media

A number of social media sites use metadata extensively and encourage webmasters to integrate with their protocols. Noteworthy metadata specifications include [Facebook's Open Graph](), [Twitter for Websites](https://developer.twitter.com/en/docs/twitter-for-websites/webpage-properties/overview), and [Pinterest Rich Pins](https://developers.pinterest.com/docs/rich-pins/overview/?). However, an important distinction exists between metadata and structured data. Of thise, only Rich Pins qualify as structured data. Open Graph metadata, which is based on RDFa, might be described as quasi-structured-data (Facebook uses the term "structured properties.").

### Publishers

Unfortunately, support for structured data is largely arbitrary and caprecious. For example, the microformats wiki claims LinkedIn marks up public profiles using [hResume](), but as of April 2019, this doesn't appear to be true. They do, however, mark up LinkedIn Learning courses using RDFa. GitHub meanwhile exposes user profiles as both microdata and microformats2 [h-card](http://microformats.org/wiki/h-card), but nowhere do they advertize the fact.

## JSON-LD

[JSON-LD] is included in a document `head` using a `script` tag with the attribute `type="application/ld+json"`. The most obvious drawback to this approach is reduplication of content--first in the JSON object, and then in the body of the document. Disparities between structured data and user-visible content are SEO felonies. So basically, the only way to safely use JSON-LD markup is in a CMS or static site generator, where the data and content are both generated from a "single source of truth."

For example, it should be straightforward to implement this approach using Jekyll, which provides a custom `jsonify` [Liquid filter](https://jekyllrb.com/docs/liquid/filters/). This mechanism could be used in a custom [layout](https://jekyllrb.com/docs/layouts/) to transform YAML front matter into a JSON object. The front matter fields would also be available in the body using Liquid tags.

## RDFa

## Microdata

The [microdata specification](https://html.spec.whatwg.org/multipage/microdata.html) is a normative part of the [WHATWG](https://whatwg.org/) version of the HTML5 standard and a [working draft](https://www.w3.org/TR/microdata/) in the W3C version. W3C also publishes a wiki article on [HTML Data Vocabularies](https://www.w3.org/wiki/HTML_Data_Vocabularies) in 

## XMDP profiles

The HTML4 standard describes a mechanism for defining new link-types, using a `profile` attribute on the `HEAD` element. The standard states that the value-type of the profile attribute is a URL, but it says nothing about the structure of the target document. [XMDP] (XHTML MetaData Profiles) is a proposed standard for HTML4 profiles. XMDP profiles are terminologies: lists of vocabulary terms and their definitions. As such, profile terms are  ideal targets for `rel="tag"` hyperlinks described in the microformats [rel-tag](http://microformats.org/wiki/rel-tag) specification.

Unfortunately, XMDP appears to be a poor interpretation of the HTML4 profile mechanism. The standard states that profiles should specify the allowable values for the link-types they define. XMDP profiles do not accomplish this. In fact, the XMDP profiles for microformats do not define new link-types at all. They define terms for use in structured data markup. But the HTML standard already defines a Glossary link-type for just this purpose.

[XMDP]: http://gmpg.org/xmdp/ "XML MetaData Profiles spec"
