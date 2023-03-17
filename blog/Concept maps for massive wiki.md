# Concept maps for massive.wiki

**Many thinking tools provide a concept map of the users' notes, either off the shelf or via plug-ins. These maps, however, won't currently appear on the web-facing version of a massive.wiki. Should they, and if so how could such multi-author concept maps work?** 

*(This post is massively incomplete. Please dont let that stop you contributing, as I've taken a permanent version snapshot (see [[#^668be5|Revision notes]]).*

A few months ago [Jerry Michalski ](https://www.jerrymichalski.com/) recommended Steven Pinker's book [
The Better Angels of Our Nature: Why Violence Has Declined](https://stevenpinker.com/publications/better-angels-our-nature) to me. It's huge, covering 1000s of years of human history in almost 850 dense pages, followed by 60 pages of notes, another 60 of references and a 50-page index. 

I found myself regretting, as I finished it, that I hadn't read it with my laptop alongside me, making notes as I go. There are just so many ideas in it, each supported by a web of data, scientific papers and other ideas, that it's impossible to hold all of it in my head. The book's notes, references and index are useful, but they're locked away in my bookshelf, not here where I need them in my notes, let alone sharable with others. 

So it got me thinking: if I was to note what I found in a book like Pinker's, could I organise and present those notes graphically via a concept map, to help me get the most out of them? And how could I share, discuss and compare my concept map with other people, given that Pinker's book has generated plenty of [opposing challenges and critiques](https://en.wikipedia.org/wiki/The_Better_Angels_of_Our_Nature#Criticism)?

In parallel, I wanted to draw up a "maturity heatmap" of the minimum viable ecosystem for decentralised collective intelligence. Could a concept map do the trick?

## User requirements

This post sets out some ideas of how that could look. While I'm not clever enough to then provide solutions, some first attempts to play with Obsidian's graph view and Juggl will eventually find their way somewhere near the end of this post.

### More than a list of notes

*Let's start with the first question, concerning mapping notes from Pinker's book.*

Firstly, the book is not a mere enumeration of ideas and their supporting facts: it provides a structure of interlocking ideas to explain downward trends in the level of violence over the past centuries . Paraphrasing Wikipedia's summary, he sets out what I'll call here **15 high-level ideas**:

* Six trends of declining violence, from the Pacification Process (from the anarchy of hunter-gatherer and horticultural societies to the first agricultural civilizations) through to the Rights Revolutions since the end of WWII
* Five inner demons: psychological systems from Predatory violence through to Ideology
* Four better angels, which despite being outnumbered seem to have gained the upper hand: Empathy, Self-control, Moral sense and Reason. 

Each idea is supported by a lot of data presented within the book, and in the form of cited academic papers. Moreover, some data supports several ideas, while occasionally he'll mention data which supports some ideas but seems to oppose other ideas. Science is like that.

### Concept maps

A good set notes from such a book would not be a useless hairball of interlocking markdown files - it should reflect this structure as well as the actual (sub)chapter structure of the book itself.

Users of Obsidian know that, unlike Roam Research, it comes with a pretty useful graph view - here's a snapshot of a graph of the notes in this massive.wiki, taken as I write this:

![[obsidian-graph-view.png]]

Obsidian's graph view presents each note as a node, bidirectionally linked, with node size representing the number of incoming links, and is filterable as shown.

But in an ideal world I'd like something like this:

![[conceptmap.png]]

In the above picture:

* each note is a node, as before
* some notes have been identified as Ideas, others as Facts
* the links between them are characterised as Supporting or Contesting - ie
	* an Idea can Support (green) or Contest (red) another Idea 
	* a Fact can Support or Contest an Idea 
	* a Fact can Support or Contest other Facts

The graph shows some links as single-headed and others as double-headed arrows, to avoid an Ideas appearing to Support a Fact. This does *not* mean that a user exploring an Idea would not see the Facts supporting or contesting it.

In an ideal world:

* such a concept map would emerge from one's notes as a force-directed graph of nodes simply by labelling notes as either Idea or Fact, and including some semantic information (Support or Contest) with the links between them. 
* you could "boost" or reposition specific nodes - if you wanted a node for each book Chapter, for example, you might want to enforce their size, and position them as I have the two largest Ideas in the above map.
* you could filter the nodes for type (Idea, Fact) and/or book (sub)Chapter and/or tag.

### Going social

A community collaborating on a set of notes should see exactly the same behaviour as an individual, but *what happens when concept maps developed separately are combined?*

Imagine two communities developing two different concept maps on the same underlying material. Then imagine an ecosystem which allows these maps to be discovered, linked, contrasted, compared and possibly even combined. How might that look?

image to do

`Pilot project opportunity? Coincidentally, shortly after I finished Pinker's book, [[Peter Kaminski]] wrangled me an invitation to an Obsidian Book Club: a community of people reading the same book, writing their notes into a Dropbox-shared Obsidian vault, and meeting every week to literally compare notes.`

### Heatmaps

*Could the same concept maps have "heatmap overlays"?*

A heatmap overlay sits semi-transparently above an existing image, adding another layer of information. 

I, for example, would love to see a "maturity heatmap" showing the technical/market maturity of the various technologies required for[ the minimum viable ecosystem for decentralised collective intelligence](https://mathewlowry.medium.com/a-minimum-viable-ecosystem-for-collective-intelligence-7738848ce9c4), which would show meat a glance exactly where resources need to be focused.

example heatmap

And then I'd love to see an array of such heatmaps, allowing me to see at a glance which ecosystem is closest to maturity.

So could the concept maps explored earlier also include heatmaps? Presumably each node would include a value for each overlay (eg something like `maturity::4`). These valuescould even be calculated from the nodes linked to it, somewhat similar to the way the spidergraph in this massive.wiki (will) present average scores for each tool for thought, calculated from the profiles of the people using it.

## Solutions (tbd)

### Obsidian graph view (available)

`What I can get from Obsidian graph view: limited to Obsidian users, invisible to website visitors`

### Juggl  (available)

`Playing wth Juggl. Same issues as Obsidian graph view? tbc`

### d3 (open source)

Could a tool be developed which could generate a d3.js file from any set of compatible markdown files, created using any thinking tool? Such a file could be integrated by the thinking tool *and* displayed on public sites.


___

## Revision Notes

^668be5

* version control (currently managed manually - see [[Wiki practice meets blogging]]) 
	* this is version: 2
	* here is the current version: [[Concept maps for massive wiki]]
	* previous version: [[Concept maps for massive wiki 1]]