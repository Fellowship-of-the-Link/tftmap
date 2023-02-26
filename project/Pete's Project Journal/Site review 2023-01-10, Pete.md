# Site review 2023-01-10, Pete

_a post in [[Pete's Project Journal]]_

I'm doing a review of the site, partly for the "Check/Complete" tasks in the task tracker, and partly with the idea to generally tidy up the site.

Some thoughts:   
- use consistent capitalization for pages
	- tools and practices may have separate rules?
- use ISO 8601 date format
- use hashtags consistently
	- see the Tags pane
- pro tip: consistency is achieved by writing down rules in the style guide (in consultation and discussion with all the participants)
- delete pages that aren't really being used (empty, deprecated, etc.)
- resolve the "front of house / back of house" issue, either by having two separate wikis (probably better), or by using something else like simple namespaces for each
- move `data` files to `_attachments`
- move `files` pages to root, get rid of `files` folder
- move `project` pages to root, get rid of `project` folder
- see "Repatterning page titles and tags" below  

## Repatterning page titles and tags

At the top of pages, rather than:

```
#tool: #pocket
```

(tag: tag)

I suggest:

```
# Pocket

#tool
```

(page title / tag)

-----
### 2023-01-15 Some thoughts and comments by [[Bill Anderson|Bill]]

Whilst trying to construct a simple and usable Massive Wiki vault I re-read this internal blog post and have some thoughts.  

- Pete's comment above "... get rid of `files` folder": perhaps it is OK in a MaSVF wiki to have a `files` folder that is the one bucket for all newly created files?  
- perhaps the simple "Repatterning page titles and tags" suggestion is a primary organizing principle?  
- and also keep an `_attachments` folder for all (all?) the non-Markdown formatted files?  

But what about all those other folders that I have created to organize my files? Yeah, that is a good question. But once I start thinking like this (one folder for Markdown files) I am reminded of the [Hugo](https://gohugo.io) framework and its directory organization for the primary `content` directory and other folders for associated non-Markdown files, and the designated `public` directory for the html webfiles. This framework has some similarities to the current MassiveWikiBuilder (MWB) model. (Note: I think the MWB framework is better for Obsidian vaults since all Markdown in the vault is rendered as HTML.)  

- none of this resolves Pete's questions about one flat file space. One flat folder for a vault will result in a very long list in the left-hand sidebar. Does this force us to rely on search and tags to find pages?
