# Wiki practice meets blogging

**What can wikis offer blogging, and vice versa, particularly in a decentralised collective intelligence environment?** 

*Preface: While you're reading the "current" version of this page, you can explore the previous versions via the Revision Notes at the end.*

Are you reading a blog post or a wiki page right now? And what's with that preface in italics, above?  

If you're reading this on the Tools for Thought Map (TfTMap) website you're reading a wiki page, whereas if you're reading this on Medium it's a blog post. The content, however, is almost identical.

That tells us something about the difference between wikis and blogs. The team driving the TfTMap pilot project explored these differences, and developed an approach for massive.wiki which simultaneously enriches blogging by adding some of the best aspects of wikis, and allows wikis to better host something resembling blogs.

## Two wiki authors and a blogger walk into a bar...

The TfTMap is a Massive Wiki pilot project, led by Massive Wiki inventors ([[Peter Kaminski]] and [[Bill Anderson]]) teaming up with [[Mathew Lowry]], a blogger since 2007. 

It was perhaps inevitable that we had a great chat on the difference in philosophy between wikis and blogging, but it started from more prosaic questions of **version control and permanence in Massive Wiki**: should previous versions of a wiki page be made available? Which ones? How? Does it matter if visitors to an old version cannot find the latest one? Who does it matter to? 

So we decided to find out by writing this page together using Massive Wiki. 

### Version control

Different CMS do **version control** differently. Most sophisticated ones use major and minor versions. Mathew's rule of thumb for his day-job, where online content is sometimes legally important and/or massively multilingual:

* if you're fixing a typo, you create a new minor version
* if you're making an editorial change large enough to warrant sending it to the translators to update any translations, you create a new major version.

### Who wrote that blog? Who's writing that wiki? 

How does this apply to blog posts and wikis?

**Wiki pages** are changing all the time - they're living documents, maintained by (hopefully) armies. They are *not* time-critical, and so are presented as part of an interconnected body of knowledge organised more by topic than creation date (how often do you visit Wikipedia to view it's "latest page"?). 

**Blog posts,** on the other hand, are supposed to be snapshots of what *one person* - the blogger, not a collective - was thinking *the very moment* they hit 'publish'. Posts are presented in a reverse chronological feed which implies Newer is Better. While they do get updates, it's a matter of honour in the blogosphere to explicitly state any 'major version' updates upfront, to avoid accusations of  surreptiously editing "*what I said 3 years ago*" to better match today's reality. With the reverse chronological presentation of blog posts, many bloggers will simply write a new post when their views change rather than update an old post few people will read anyway.

As a blogger, Mathew found writing a new post just to update an old one a pretty bad solution: after all, the old one remains online, unchanged and now an innacurate representation of the blogger's views. Of course s/he could update the old post to add a link point to the new one... but when there are 5 versions they'll all need an  update when s/he wants to add a sixth.

It turns out that the same basic solution serves both wikis and blogs.

## Canonical blog posts 

Better, perhaps, to have **a canonical blog post which always sets out the current version of *"what I think about this thing"***. 

The canonical version's URL would never change, but its content can: before an author makes a significant change as their understanding evolves, s/he creates a **permanent version**: a copy of the blog post that serves as a shapshot of it before the editing begins. 

![[permanentversioning.png]]

To ensure visitors can see how the post evolved, the canonical post must link back to the most recent permanent version, which in turn links back further. And each permanent version should point forward (at least) to the canonical version, for people who discover a permanent version via search engines.

## Blogging in a wiki

Wiki sites tend to not feature blogs, as bloggers are often reticent to write a blog post on a platform where other members can edit it. That's a shame, as there are a lot of bloggers out there who could add their ideas to collective intelligence sites if they felt their authorship was better acknowledged.

Permanent versions square that circle, allowing the blogger to:

* post their piece, and then create a permanent version
* see the canonical version evolve from "*what I think*" into a text representing the community's collective intelligence
* while still being able to point to "*this was what I originally wrote*".


## How would this look in practice?

In Massive Wiki, Git manages every version of every file, committed by each contributor, ideally with the contributor's comments (the end March 2023 major update, for example, was accompanied by "*permanent version blogpost - new version for wider consumption*"). 

While these "Git commit comments" *can* indicate which updates are minor and which are major, they are not visible to site visitors, although they can be accessed on github if the repository is public (see the [TfTMap GitHub repository](https://github.com/Fellowship-of-the-Link/TfT-test1/commits/main)). 

While Git fulfils the requirements for managing minor versions off-the-shelf, therefore, major version changes need to be better signalled to visitors by the editors on the site content itself. How might that look? 

### A "create permanent version" button

Ideally, we'd build a "first class function" for Massive Wiki for making a new major version of a file. With one click, this function:, applied to version "N" of a file:

* increments its version number to "N+1". This file remains the "active" or current version of the file, available at the original, unchanged URL.
* creates a copy of version "N" in an archive folder, applying the permanent copy template. This permanent copy of version "N": 
	* has the version number and creation date appended to the filename (eg *Wiki practice meets blogging-N-YYYYMMDD*).
	* includes a link to forward to the current version of the file, a "search for all versions" feature, and an explanatory "this is a snapshot" label.
* adds a link from the current version of the file to the newly created permanent version (ie, the current "N+1" version of the file links back to "N"). As this link is kept when a new permanent version is created, a chain links each file to the next older version ("N" links back to "N-1", and so on).

The main problem I see here is that the Editor must decide to create a major version **before starting editing**, not after having worked on the content.

### Mimicking this manually

While a first class function would be nice, it's very easy to do manually, as set out in detail in [[Manually creating permanent versions on this wiki]]. In brief, the creation of a major version entails the following manual processes:

* creating a copy and moving it into a "permanent versions" subfolder
* editing two lines in the new permanent version and adding a preface signalling that it's not the current version
* editing one line in the current version

Simple!

---

## Revision Notes

* 2023-03-29: new version created, cleaned up for reposting to Medium
* version control 
	* this is version: current
	* here is the current version: [[Wiki practice meets blogging]]
	* previous version:  [[Wiki practice meets blogging 5 2023-03-30]]

