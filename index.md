---
title: Developer Profile Development
author: "Mark Tippetts"
---
As a developer with a particular interest in the Semantic Web, it makes sense to have a GitHub profile that's designed to work with these technologies. In practical terms, this means working with [structured data]({% link structured-data.md %}): a way of embedding metadata in HTML markup, for use by search engines and content aggregators. A number of competing structured data formats exist, including JSON-LD, RDFa, microdata, and microformats. It's also necessary to decide on a data model, which may be expressed in a controlled vocabulary, schema, or ontology.

An obvious choice is the microformats2 [h-resume](http://microformats.org/wiki/h-resume) specification. Unfortunately, this spec doesn't seem to be supported by any major publishers or consumers. The specification page, which lists known implementations, hasn't even been updated since 2013. That would be enough to disuade most people. But as a Semantic Web developer, I'm no stranger to toiling in obscurity. So what the heck? Maybe I'll use it anyhow! But before committing to a specific format or schema, it seemed like good idea to see what others are doing. So I conducted a survey of [prior work in this area]({% link existing-work.md %}) in order to develop a clear understanding of the alternative content models.

Finally, all this seemed like an awful lot of effort to go to, just for one web page. So as long as I was at it, I thought I might publish the fruits of my labor in a tool others can use.

The question was, how? The easy answer would be to create a [Jekyll plugin](https://jekyllrb.com/docs/plugins/). Unfortunately, for security reasons, GitHub Pages doesn't allow using 3rd party gems, with the exception of theme gems. There is a workaround for this: Rather than having the GitHub Pages build-engine do the work, you can build the site locally and upload the results. But that would break tools like Prose and NetlifyCMS that work with GitHub sources.

In light of this restriction, and since layout templates will figure significantly in the list of work products, a [Jekyll theme](https://jekyllrb.com/docs/themes/#creating-a-gem-based-theme) seems like an appropriate distribution format.

An apparent problem with this is that it locks potential adopters into using whatever styles I choose, which defeats the whole point of having a themeable site generator. So perhaps a simple starter project would be more appropriate? Or maybe there's some SASS-y trick I could use to work around the stylesheet lockin issue? Since I've always been much more focused on questions of data modeling and navigation than the more aesthetic aspects of design, there's a lot I don't know about the CSS ecosystem. If there's a way of applying a kind of object-inheritance polymorphism to theme selection, that could be a very cool trick.

That's definitely something to look into. But meanwhile, I wanted to get to work. So on [the principle](https://blog.codinghorror.com/the-last-responsible-moment/) that you should "never decide today what you can put off until tomorrow," I've gone ahead and initiated the project as a Jekyll theme. It's a difference of deleting one file if I change my mind.

## Content models

## Content management

The CMS could use GrapesJS for developing templates and Jekyll-Admin or Prose for populating them.

- A set of [configuration defaults] and [field descriptors] is derived from each content model for managing records.
- A Jekyll (Liquid) template is derived from each content model for displaying records.

## Theme management

[Netlify version](https://matippetts.netlify.com) of this site  
[Netlify-CMS admin](https://matippetts.netlify.com/admin)

- My CV
- My portfolio of Open Source projects and code samples
- Unpublished project repositories
- Ideas for future projects
- My [agenda]({% link learning-goals.md %}) for learning new technologies
