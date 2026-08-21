# Overview Page Style Guide

Guidance for writing/rewriting section overview pages on the Joomla User
Guide (https://guide.joomla.org/). Derived from analysis of three pages
judged "good examples" (see `examples/`): Getting Started (298), Articles
(299), and Fields (369). Living document — update it as new sections
surface new cases, and note any open questions inline until resolved.

## Structure

1. **Intro** — one to three short paragraphs before any heading. Explain
   what the section covers and why it matters, in plain language. Length
   scales with section size: a couple of sentences for a small section,
   up to a few short paragraphs for a large one (see Articles/298 example).
2. **Subsections** — only for sections with enough articles that a flat
   list would be hard to scan (roughly 6+ articles, or articles that fall
   into distinct natural groups). Each subsection gets:
   - an `<h2>` heading naming the subsection
   - one short sentence (sometimes a full paragraph) introducing it
   - a `<ul>` of article links
   Small sections (a handful of articles or fewer) skip subsections
   entirely — just the intro followed by one flat `<ul>`. This includes
   sections with only a single article: still write a real intro and a
   one-item `<ul>` rather than dropping the list, for consistency with
   every other overview page.
3. **Article links** — one `<li>` per article:
   ```html
   <li><a href="user-manual/section-slug/article-slug">Article Title</a> – Brief description.</li>
   ```
   - **Link text** matches exactly what appears in the left-navigation
     menu module on guide.joomla.org - not necessarily the article's own
     page title/heading, which can differ (e.g. the menu says "Keep
     Submenus Open" while the article itself covers more ground). When
     in doubt, check the actual rendered menu rather than an article's
     title or an overview-page table, which can render link text
     differently (lost casing, truncated wording, etc.).
   - **Description** is 1–2 sentences that expand slightly on the title
     and tie it back to the section/subsection it's in — not a repeat of
     the title, not a full summary of the article.
   - **href** is relative to the guide root (no `https://guide.joomla.org`
     prefix) — matches all three examples.

## Markup cleanliness

Keep markup plain. Two of the three examples (298, 299) carry over
`dir="ltr"`, `aria-level="1"`, `role="presentation"`, and an extra wrapping
`<p>` inside each `<li>` — artifacts of pasting from Google Docs, not
intentional formatting. The third example (369) has the cleanest structure:
```html
<li><a href="...">Title</a> – description</li>
```
Prefer 369's plain structure for new/rewritten pages. Don't introduce the
dir/aria-level/role attributes or the extra `<p>` wrapper.

## Dash style

Use an en dash (`–`) between link and description, e.g.
`<a href="...">Title</a> – description`. (298 and 299 already use en dash;
369 uses a plain hyphen — treat that one instance as the exception, not the
model, and use en dash going forward.)

## Spelling: British English

Default to British spelling whenever it differs from American English —
e.g. *organise* (not organize), *colour* (not color), *customise*,
*centre*, *catalogue*, *licence* (noun) / *license* (verb), *favourite*,
*behaviour*, *synchronise*. 369_Fields already does this ("Colour Field"),
so this is consistent with existing practice, not a new convention.

Exception: when prose refers to an exact on-screen label, button, or field
name from the Joomla software itself, match what the software actually
shows verbatim, even if the software's own UI happens to use American
spelling. The reader is matching your words to their screen — don't let
British spelling silently diverge from what's in front of them.

## What NOT to do

- Don't pad descriptions into full explanations — one to two sentences.
- Don't invent subsection groupings that don't reflect how the articles
  actually relate; when in doubt, ask before restructuring.
- Don't use full `https://guide.joomla.org/...` URLs in links.
