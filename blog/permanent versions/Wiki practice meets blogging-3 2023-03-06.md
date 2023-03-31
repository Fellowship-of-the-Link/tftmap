# Wiki practice meets blogging

`This is a permanent version, or snapshot, of this page. Please see Revision notes, below, for more details.`

## About this page

*ML:* we ([[Mathew Lowry]],  [[Peter Kaminski]], [[Bill Anderson]])  had a great chat as we prepared version 1 of this site on the difference in philosophy between wikis and blogging. We decided to write something together on it using Massive Wiki, to explore the issue by writing about it and to test he various collaboration Contribute and Commenting options we are proposing to this site's contributors. Key links:

* this page is being discussed on Mattermost: https://chat.collectivesensecommons.org/agora/pl/cjjtx46exjrh3czajguek3r6ur
* it can also be commented on and developed according to the ideas set out in [[How to comment]]

*ML:* I am keenly aware, as I write this opening paragraph of this newly created page, that **I'm writing this like a blog post** -  for one thing, I'm labelling each paragraph as 'mine', which is a very blogger* thing to do (* a polite way of saying 'author egocentric'). By the time we show this to more people, however, this content will have been **wikified through collaboration**, and this paragraph may be gone. 

*ML:* But not, perhaps, forgotten - there may be an early version of this page kept somewhere, because our discussion started when we considered *version control and permanence in Massive Wiki*: should previous versions of a wiki page be made available? Which ones? How? Does it matter if visitors to an old version cannot find the latest one? Who does it matter to?

## *ML:* Version control

Different CMS do **version control** differently. Most sophisticated ones use major and minor versions. My rule of thumb for my day-job context, where online content is sometimes legally important and/or massively multilingual:

* if you're fixing a typo, you create a new minor version
* if you're making an editorial change large enough to warrant sending it to the translators to update any translations, you create a new major version.

But what of a wiki, and what about blogs? Wiki pages are changing all the time - they're living documents, maintained by (hopefully) armies - whereas blog posts are supposed to be snapshots of what the blogger was thinking *the very moment* they hit 'publish'. 

### Exploring version control & permanent copies with this page

Co-editing this page will hopefully surface an answer. To launch and explore that discussion, I'm:

* writing everything down I can think of, preceded by [ML] in case it helps organise the conversation to come (and because I'm a blogger, for whom bylines often matter)
* adding a Revision Notes section to the bottom, as agreed for the site as a whole
* pushing the first version of the page to the site
* creating a new major new version of the page and linking the two together following the manual version control system set out below, and pushing that too before opening this for discussion. Briefly:
	* The idea is that each new major version will create a new (Vx) file linking back to (V-1)x , creating an unbroken chain backwards in time - something I'm borrowing from [[Gordon Brander]]'s [[subconscious]].
	* But I want to minimise the manual editorial workload until a feature is developed


### *ML:* Blog posts

Of course, blog posts do get updates, but in the blogosphere it was always a matter of honour to explicitly state any 'major version' updates upfront, to avoid accusations of  surreptiously editing "what I said 3 years ago" to better match today's reality. With the reverse chrono presentation of blog posts, many bloggers will simply write a new post when their views change rather than update an old post few people will read anyway.

Personally, as a blogger, I find writing a new post just to update an old one is a pretty bad solution: after all, the old one remains online unchanged. Of course I could add a quick update to the old post pointing to the new one... but what happens when I have 5 versions of the same post? When I add a sixth I'll have to update all 5 manually!

Better, perhaps, to have **a canonical blog post which sets out the current version of "*what I think about this thing*", date-stamped with the last major version,** with an auto-link back to previous versions. Ideally all previous versions auto-link not just backward, but also forward to both the next and canonical versions. 

## Wiki pages

*ML:* The above applies to blog posts because blog posts are (usually) written by a single author and are presented in a reverse chronological feed which implies Newer is Better. Wiki pages, on the other hand, are collaborative efforts where the authorship can be almost impossible to track. 

*WLA (2022-12-11):* It seems to me that on wikis the authorship is not as important as the text of the wiki pages, and, perhaps, how well that content is written and cited.

*ML:* They are also not time-critical in nature and so are presented as part of an interconnected body of knowledge organised more by topic than creation date (how often do you visit Wikipedia to view it's "latest page"?). 

So how would version control and permanent versions look like in this context?

tbc

## Combining blogs and wikis

*ML:*  How would a site which combines wikis and blogs look?

tbc

## Massive Wiki user requirements

*ML:*  In the current version of Massive Wiki, Git manages every version of every file, committed by each contributor, ideally with the contributor's comments. While these "Git commit comments" *can* distinguish between new versions submitted to fix a typo and versions which totally transform the page's contents, they are not visible to site visitors, although they can be accessed on github if the repository is public (see [this site's](https://github.com/Fellowship-of-the-Link/TfT-test1/commits/main)). 

*(Note that this does not factor in possibilities offered by GitHub such as branches, which provide something intermediate between minor and major versions.)*

*ML:*  Personally, I think Git fulfils the requirements for managing minor versions off-the-shelf, but major version changes need to be better signalled to visitors by the wiki's editors on the site content itself. How might that look? 

### Designing a first class function

*ML:* In our chat we discussed a "first class function" for Massive Wiki for making a new major version of a file. With a click:

* the version number of the file being edited is increased by 1, but remains the "current" version of the file, available at the primary URL (this one is "*domain/blog/The Way of the Wiki meets blogging*") 
* a copy of the file is created in an archive folder, becoming the permanent copy of the previous version. It's filename includes the current version's filename appended with the version number and the creation date.
	* Q: does it need a hash as well?
* a link to the previous version is added to the current version (site feature)
* all permanent copies can easily feature:
	* a link to the current version (this is fixed at the first version, so doesn't need to be updated manually)
	* a "search for all versions" (site feature: part of the permanent copy template) 
	* an explanatory "this is a snapshot" label - see for example wikipedia's view history  (site feature: part of the permanent copy template)

One problem I see here is that the Editor must decide to create a major version **before starting editing**, not after having worked on the content.

### Mimicking this manually

*ML:* Note that almost all of the above can be done easily manually, which is what we'll have to do for this file and any other blog posts on this wiki. 

How is set out in detail in [[Manually creating permanent versions on this wiki]]. In brief, the creation of a major version entails the following manual processes:

* creating a copy and moving it into a "permanent versions" subfolder
* editing two lines in the new permanent version
* editing one line in the current version


---

## Revision Notes

* (29/01/2023) extracted and generalised [[Manually creating permanent versions on this wiki]] to make this page more readable
* version control (currently managed manually) 
	* this is version: 3
	* here is the current version: [[Wiki practice meets blogging]]
	* previous version:  [[Wiki practice meets blogging 2 2023-01-29]]

