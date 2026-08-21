# Git Sync Workflow (User Guide)

Adapted from `AI_Workspace/Tutorials/Git Sync Workflow.md` (written 2026-07-25)
— same repo, same conventions, applied to overview pages instead of tutorial
articles. Written 2026-08-21.

## The problem this solves

Content moves between three places: Joomla (the live site), this working
folder, and whatever Claude just edited. Git turns the folder into a
timestamped, diffable history — the answer to "who has the latest copy"
becomes "check the log" instead of "try to remember." This matters
especially here because Joomla is multi-user: another editor could change
a live overview page between our sessions without telling Claude.

As of 2026-08-21 Claude has read/write access to the full `JoomlaDocumentation`
repo root (not just this folder) — the same "future upgrade option" the
Tutorials doc mentions. Even so, by Jeff's preference Claude does not run git
commands directly: Claude edits files and drafts commit messages, Jeff runs
`git add` / `git commit` / `git push`. Paths below are relative to the repo
root, e.g. `AI_Workspace/User Guide/...`.

## The three kinds of commits

**1. Sync from Joomla** — whenever Jeff copies fresh HTML out of the Joomla
article editor and pastes it into `overview-pages/<id>_<Title>.html`
(whether untouched or someone edited it live), that's a commit *before*
asking Claude to touch the file. Use the version timestamp from Joomla's own
article version history:

```
Sync from Joomla: 298 Getting Started (Joomla version 2026-08-15 10:22:04)
```

**2. Claude's edits** — after Claude finishes a meaningful change, Claude
writes the commit message to `AI_Workspace/User Guide/commit-message.txt`
and gives Jeff the command:

```
git add -A
git commit -F "AI_Workspace/User Guide/commit-message.txt"
git push
```

**3. Pushed to Joomla** — after Jeff pastes the updated HTML back into
Joomla and saves, a short commit marks the loop closed:

```
Pushed to Joomla: 298 Getting Started (confirmed via Joomla version history)
```

## How to tell who has the latest copy

Run `git log --oneline -10` in the `JoomlaDocumentation` folder (not this
subfolder).

- Top commit is a **Sync from Joomla** or **Pushed to Joomla** commit →
  local and Joomla match, safe to hand to Claude or consider done.
- Top commit is a **Claude edit** with nothing after it → local is ahead of
  Joomla, needs to be pasted back in.
- Not sure if someone changed something directly in Joomla without telling
  Claude → re-copy the HTML from Joomla and commit a fresh "Sync from
  Joomla" before asking Claude to edit again. Git can't detect this on its
  own — this is the one place that still relies on remembering to re-sync.

If you'd rather Claude check state itself, it now has direct read access to
`git log` / `git status` / `git diff` in `JoomlaDocumentation` — just ask.

## Commit messages: use a file, not `-m`

Commit messages often quote literal UI text (menu labels, article titles),
which breaks `git commit -m "..."` the moment the message contains a double
quote. Claude writes each message to
`AI_Workspace/User Guide/commit-message.txt` instead:

```
git commit -F "AI_Workspace/User Guide/commit-message.txt"
```

No escaping, no picking quote types. The file gets overwritten each time a
new commit is ready; once committed, its old contents are preserved in git
history.

## Git command cheat sheet

Run these from inside `JoomlaDocumentation` (or any subfolder — git finds
the repo root automatically).

| What you want to do | Command |
|---|---|
| See what's changed since the last commit | `git status` |
| See the actual line-by-line changes | `git diff` |
| Stage a specific file | `git add "AI_Workspace/User Guide/overview-pages/298_Getting_Started.html"` |
| Stage everything that changed | `git add -A` |
| Commit staged changes with a message | `git commit -m "Your message here"` |
| Send commits to GitHub | `git push` |
| Get the latest from GitHub | `git pull` |
| See recent history | `git log --oneline -10` |
| See what changed in one commit | `git show <commit-hash>` |

## Reference vs. working files in this folder

- `examples/` — reference "good" overview pages (298, 299, 369). Not edited,
  not part of the Joomla sync loop.
- `overview-pages/` — the active sync loop: one file per section.
- `style-guides/*.md` and `glossary.md` — internal working documents for our
  own drafting consistency. Not believed to be published as Joomla articles
  themselves (unlike Tutorials' Style Guide / Glossary of Terms, which ARE
  live articles) — confirm with Jeff if that changes.
