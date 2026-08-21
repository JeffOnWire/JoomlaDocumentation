# Joomla User Guide — Overview Pages Project

Working folder for rewriting the section overview pages on the
[Joomla User Guide](https://guide.joomla.org/). Paired with the project's
Claude session, which reads the live menu/articles from guide.joomla.org
but writes and maintains overview-page HTML here for manual paste into the
Joomla article editor.

Part of the `JoomlaDocumentation` repo, alongside the `Tutorials` subproject.
See `Git Sync Workflow.md` in this folder for how work moves between Joomla,
this folder, and GitHub — the conventions here mirror the ones already
established for `Tutorials`.

## Folder structure

- `examples/` — reference overview pages already considered "good" examples
  (Getting Started, Articles, Fields). Not for editing; used as style models.
  Not part of the Joomla sync loop.
- `overview-pages/` — working drafts of section overview pages, one file per
  section, named `<article id>_<Title_With_Underscores>.html` to match the
  Joomla article id and title (e.g. `298_Getting_Started.html`). This is the
  active sync loop — see `Git Sync Workflow.md`.
- `style-guides/` — Markdown style guides (overview-page style guide first,
  others as they're developed). Internal working documents, not published
  as Joomla articles (unless that changes — confirm with Jeff).
- `glossary.md` — glossary of terms, for consistency across the user guide.
  Same status as `style-guides/`: internal, not (currently) a Joomla article.
