# Parsing profile pages

We'll use this page to discuss and design how we parse profile pages.  This is a work-in-progress; please improve.

## Parsing Markdown with mistletoe

Since profile pages are Markdown, we'll use the [[mistletoe]] parser to read the page into an abstract syntax tree (AST)).  This represents each component of the document (header, list item, paragraph, etc.) as an object.

Mistletoe has taken care of understanding all the Markdown syntax, and we are left with a list of items which is conceptually like this (item type, plain text of the contents of the item):

```
h1, Mathew Lowry
p, One of the [[People]].
h2, About me
p, ...
p, ...
h2, My ideal thinking tool(s)
p, ...
p, ...
h2, My current tools and practices
list
    li, I use  [[inbox curation]] to identify high-priority sources of content: in [[gmail]] I auto-label high-priority [[newsletter]], and I maintain a [[twitter list]]
    li, I use [[GTD]]: I have recurring [[calendar]] items and tasks to [[scan]] priority sources; [[queue]] the best content to read to [[Pocket]]; read, [[annotate]] and [[tag]] the best content into [[myhub]]
```

(For a complete example tree, see [[Mathew Lowry-20230212.ast.txt]].)

About lists and list items: the AST represents lists as one item that contains list items. Nested lists will be nested in the AST. (This is Good News™️.)

The mistletoe AST parser doesn't know about wikilinks. There is a [Massive Wiki parser addon for mistletoe](https://github.com/peterkaminski/massivewikibuilder/tree/main/mistletoe-parser) that does know about wikilinks, but we probably won't use it; we'll probably just use a regex that will find the wikilinks in the text, and return them in plain text. (That's similar to what the Massive Wiki addon does, except that it also knows how to output the corresponding HTML. We don't need the HTML.)

## Deconstructing a Profile Page

We'll have code that knows how to traverse the list of items to find each of the kinds of information we want; and which pages to put each of those kinds of pieces of information into.

Here is pseudocode that describes the high-level process to deconstruct a profile page.  This is a work-in-progress; please improve.

In the following, when skipping items, handle the case that there may be zero items that need to be skipped to reach the next step of the workflow.

1. For all pages in the `map` directory, convert the page to an AST.
2. In each page, if the paragrah after the H1 header contains `[[People]]`, assume this is a profile page. Otherwise, skip this page.
3. Skip items until you find an H2 header that contains `My current tools and practices`.
4. Skip items until you find a list.
5. Read each list item in the list, pull out the wikilinks, and save the list item into an array of `tools_or_practices`. Create one item in the `tools_or_practices` array for each wikilink, and index the item by the wikilink.
6. Skip items until you find an H2 header that contains `Thinking Tool Ratings`.
7. Skip items until you find a list.
8. At level 0 of the list, save the content of the list item as the name of a tool.
9. At level 1 of the list, you'll find `(text): (number)`. Save the number as the score for the dimension indicated by the text. There may be a special dimension, `My current confidence with this tool`.
10. At level 2 of the list, you may find notes related to this dimension/score. (Pete asks, what should we do with these notes?)

## Saving the Data to the Correct Pages

TBD: the workflow to save the data gathered in the deconstruct workflow above into the correct pages.

One question (by Pete): We'll end up with an array called `tools_or_practices`.  The code can't tell if a particular item is a tool or a practice by parsing the page, because there isn't a set structure; the sentences are freeform English.

Therefore, to put the items in the right place, we'll do something like:

1. Check for an existing page by the name of the item. If it exists, it is either a tool or practice (by inspection of the first link), so then handle it as such.
2. If the page doesn't exist, create a new page in a working folder called `Tools or Practices`, and do the best you can writing the data into the page.  (Perhaps write the data as a tool, then a separator, then as a practice.) Add the name of this page to a to-do list for human gardeners to move and format into either a Tool or Practice page.