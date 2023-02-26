# Profile parsing update, 2023-02-25

_a post in [[Pete's Project Journal]]_

I've been working on code to implement [[Parsing profile pages]]. The parsing part is pretty much done, and it parses the [[Mathew Lowry]] and [[Aram Zucker-Scharff]] pages handily. (I'd been using Mathew's page for testing and development, and then tried Aram's page, and it worked with no changes to the code!)

Flancian's, Bill's, and Pete's pages throw errors because of missing sections or something, but that shouldn't be too hard to fix in the code.

I updated the [[Tools]] and [[Practices]] pages by running the parser on all those Profile pages, which automatically found all the [[torps]] (tools OR practices).  I did some manual cleanup, then manually sorted the list into each of the Tools or Practices pages.

I'm now starting to work on what to do with the parsed data.

One of the key things the code needs is to know whether a torp is a Tool or a Practice, because different things are done with the data for each.  I think what I'll do is have the code read `Tools.md` and `Practices.md` to know which is which, before parsing all the Profile pages.  If it finds torps that are not already in one of the lists, it probably will output a warning for humans to add the torp to one or the other lists.

Also, if it finds a torp in _both_ the Tools and Practices pages, similarly, it'll output a warning.

Another thing to figure out: how to merge the static content (human-written) and dynamic content (as created by the code) on Tool and Practice pages.  The slickest way might be to write the dynamic content to a separate page (e.g., `Obsidian - who, how.md`) and then transclude (embed) that page onto the tool page (e.g. `Obsidian.md`).  To make that work, we'd have to implement transclusion in [[Massive Wiki Builder]], something that's not impossible, but not particularly easy -- especially because we're working on swapping Markdown processors right now.