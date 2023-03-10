# Social knowledge graphs for collective intelligence

**A personalised, decentralised Social Knowledge Graph for each user multiplies the knowledge available to them via a trusted network of Followers and Friends, and creating collaborative possibilities more akin to wikis than blogging.**

![[ecosystem-social.png]]
*Two parts of a [[A Minimum Viable Ecosystem for collective intelligence|larger ecosystem]].*

This is one of several posts exploring how a decentralised ecosystem for collective intelligence could be bootstrapped into existence. As set out in the introduction to the series ([[A Minimum Viable Ecosystem for collective intelligence]]), I’m exploring these questions by re-imagining how MyHub.ai could evolve into an open-source toolkit positioned within a decentralised, open-source and self-sustaining ecosystem for collective intelligence.

In [[Thinking and writing in a decentralised collective intelligence ecosystem]] I set out the minimum features required for the MyHub content management system: essentially a super-simple Tool4Thought designed to help Editors not just manage their Library of interlinked notes, but also to develop them into articles to publish on their Hub, newsletter, digital garden or other public website.

**But what happens when Editors can also form and access Social Knowledge Graphs, integrated into their Tool4Thought?** This post builds on the previous one to explore how social features could allow Editors to:

- discover new content, and through them the person who published it and others who valued it
- create trusted networks for sharing notes and unfinished drafts
- collaborate on ideas with people they trust
- create subscription services for paying customers.

## Social network: Followers and Friends

The figure at the top of this post is extracted from the figure on my [[A Minimum Viable Ecosystem for collective intelligence|introductory post]]. It shows MyHub Editors have two types of social link:

### Followers

The Followers relationship is, like Twitter’s, asymmetrical:

- If you Follow someone, they become a Priority Source (everything they publish appears in your Inbox — see [Thinking and writing in a decentralised collective intelligence ecosystem](https://mathewlowry.medium.com/thinking-and-writing-in-a-decentralised-collective-intelligence-ecosystem-16dd2b1893cc))
- If they Follow you, everything you publish appears in _their_ Inbox
- But just because you Follow them does not mean they Follow you.

### Friends

The Friends relationship is symmetrical: you can _propose_ to be someone else’s Friend, but they must agree for the relationship to exist. This is because it is far more trust-driven - you can make some of your Library content accessible to your Friends, and vice versa, allowing you to:

- share your thinking with your Friends
- work together on shared content
- create subscriber-only content: ie, monetise some of the Notes and Overviews in your Library by making it available to those paying a subscription or even per-article fee.

Editors can also categorise their Friends into Groups, and so make some Library content visible to a subset of their Friends, or make a specific piece of Library content visible to an _individual_ Friend. On the other hand, an Editor can set _all_ their Library content to public by default, eschewing a Private Library and permanently “[working with the garage door up](https://notes.andymatuschak.org/z21cgR9K3UcQ5a7yPsj2RUim3oM2TzdBByZu)”.

The above relationships, of course, exist between nodes in a totally decentralised network of independent domains. There are a number of technical options and many more under development. The most obvious starting point would be to put every Hub on the Fediverse by integrating an ActivityPub account creation process into the public Hub template.

Each Hub would then be able to easily Follow any other Hub _and_ any other account published using the ActivityPub W3C standard (Mastodon, Friendica, etc), while users of those tools could easily Follow any Hub. Instead of creating a separate universe of Hubs, in other words, the universe of Hubs would seamlessly integrate into the larger Fediverse.

## Concentric circles of collective intelligence

The above relationships expand each Editor’s content universe. In practical terms, Editors exploring their Library can search and use just their Library’s content and/or the published content of the Hubs they Follow, and/or the notes shared by their Friends (both their Friends’ original thoughts, and their notes on _other_ peoples’ content).

Each user’s Social Knowledge Graph is thus their personal Knowledge Graph, connected via a writing-oriented Tool4Thought to the Knowledge Graphs of those whose opinion and judgement they respect. The resulting universe of high-quality content is therefore arranged in concentric circles:

![[concentricCirclesOfCI.png]]
_Concentric trust circles of collective intelligence, from [[Building collective intelligence from social knowledge graphs|an earlier post]]_

When the ecosystem’s [[How Artificial Intelligence will finance Collective Intelligence|AI services]] help Editors publish and describe this content using Linked Data, the curation efforts of millions of people, whose own credibility depends on the content they curate, will create a new layer of added value onto the wider web, combining the curated web with trust-driven social networks:

>“***With tools like Notion, Airtable, and Readwise … people are aggregating content … reviving the curated web. But these are mostly solo affairs… fragmented, poorly indexed… Rather than try to organize the world’s information… (we should)* organize the world’s trustworthy information**” - [The Future of Search Is Boutique](https://future.com/the-future-of-search-is-boutique/?mkt_tok=MzgyLUpaQi03OTgAAAGEPjuppI8L9CFq6RP-_zW0-4q9gO5twAjQgJaGvO8w3JN5przTVmD6cB9fPqr-pntXtjB0TQKjq-cAOk-x4i7A2wzo5cf7REpCVeJfqLfE8wmg)

## From sharing to collaboration

**The above socially extended content universe provides an environment which can support content collaboration, not just sharing.**

This section explores a few examples, but as the toolkit will be open source many more will follow. All examples are based on the following scenario: _Editor B discovers in her Inbox a note published by someone they Follow (Editor A)._ 

In addition to integrating it into her own Library (see [[Thinking and writing in a decentralised collective intelligence ecosystem#Welcome to your Library|Welcome to your Library]]), she can also:

### Reblog it as a fast endorsement

As in the eponymous feature on Tumblr, Editor A’s content card appears on Editor B’s public Hub and is pushed to B’s followers. If it was an original post by Editor A, the card links to it; if Editor A curated it, the card links to the same URL Editor A pointed to, but Editor A’s domain is mentioned.

This is a fast endorsement: Editor B is not adding any value beyond including the note in her Library and publishing it to B's Followers.

### Fork it

When Editor A’s note is forked by Editor B, the original note appears in Editor B’s library, where she can edit and eventually publish her version of it on her Hub. Forked posts are still linked to the original post, and a Friend relationship is proposed between the Editors if it didn’t already exist

Forking a post is thus Editor B’s way of acknowledging and multiplying Editor A’s content, while adding her own views. It results in two linked posts where those two views can be contrasted and compared. But linking these two posts in this way also unlocks one more possibility:

### Propose a Federated wiki post

Instead of forking Editor A’s post, Editor B can propose to Editor A that they create a shared “federated wiki” post ([#fedwiki](https://myhub.ai/@mathewlowry/?quality=all&tags=fedwiki&timeframe=anytime&types=like&types=do&types=think)).

If Editor A agrees, Editor B is added to the original post as a contributor, and can edit it. If the post is public, a note to that effect appears in the post, linking to Editor A’s Hub. This process can also happen after a post has been forked, reconsolidating two forked versions of a post.

## People and content discovery

The above features support two more key processes in building collective intelligence, each mirroring the other:

- **discovering people via content**: discovering a piece of content means discovering interesting people: both the person(s) who published it and other people who also valued it, along with what _they_ thought of it
- **discovering content via people**: having discovered someone interesting, you can discover the content they published, found interesting, etc.

While this will happen simply through the use of via decentralised, open technologies like ActivityPub and WebMentions, the ecosystem’s AI services will turbocharge both, helping people interested in the same topics discover each other.

## Dig deeper

Which brings me to the final post in this series: [[How Artificial Intelligence will finance Collective Intelligence]]. 

The rest of the series:

- The “executive summary”: [[A Minimum Viable Ecosystem for collective intelligence]]
- The first post in the series: [[Thinking and writing in a decentralised collective intelligence ecosystem]]

The site you're reading this on, finally, is the focus of our first pilot project: see [[About this project]] or [the announcement post on Medium](https://mathewlowry.medium.com/mapping-tools4thought-using-collective-intelligence-tools-9b5cd00a6309).

Comments welcome on all of them ([[How to comment]]), along with any contributions to the map ([[How to contribute]]).

  \- [[Mathew Lowry]]
  
---

## Revision Notes

* Version 1 finalised on 1/1/2023 and [reposted to Medium](https://mathewlowry.medium.com/social-knowledge-graphs-for-collective-intelligence-75c436889320) as a permanent version (see [[Wiki practice meets blogging]]).
