# Git Sync Workflow

How Jeff and Claude keep the working folder, git history, and live Joomla site in sync. Written 2026-07-25 — read this first if you've forgotten how this works.

## The problem this solves

Content moves between three places: Joomla (the live site), this working folder, and whatever Claude just edited. Without a record, there's no way to know which one currently has the "latest" version of an article. Git solves this by turning the folder into a timestamped, diffable history — the answer to "who has the latest copy" becomes "check the log" instead of "try to remember."

Claude's access is limited to the `Tutorials` folder. The actual `.git` repo root is one level up, at `JoomlaDocumentation`, so **Claude cannot run git commands directly** — Jeff runs them, using commit messages Claude provides.

## The three kinds of commits

**1. Sync from Joomla** — whenever Jeff copies fresh HTML out of the Joomla article editor and pastes it into a file here (whether it's untouched or someone edited it live), that's a commit *before* asking Claude to touch the file. Use the version timestamp from Joomla's own history (visible via the article's version history link) in the message:

```
Sync from Joomla: CM7.4 Restrict Access to Articles (Joomla version 2026-06-12 16:28:36)
```

**2. Claude's edits** — after Claude finishes a meaningful change or batch of changes, Claude writes the commit message to `Tutorials/commit-message.txt` and gives you the command:

```
git add -A
git commit -F "Tutorials/commit-message.txt"
git push
```

**3. Pushed to Joomla** — after Jeff pastes the updated HTML back into Joomla and saves, a short commit (often just touching a tracking note, or simply noted in the commit message of the next sync) marks that the loop is closed:

```
Pushed to Joomla: CM3, CM3.1-3.5 (confirmed via Joomla version history)
```

## How to tell who has the latest copy

Run `git log --oneline -10` in the `JoomlaDocumentation` folder (not `Tutorials`).

- Top commit is a **Sync from Joomla** or **Pushed to Joomla** commit → local and Joomla match, safe to hand to Claude or consider done.
- Top commit is a **Claude edit** with nothing after it → local is ahead of Joomla, needs to be pasted back in.
- Not sure if someone (you or a colleague) changed something directly in Joomla without telling Claude → re-copy the HTML from Joomla and commit a fresh "Sync from Joomla" before asking Claude to edit again. Git can't detect this on its own — this is the one place that still relies on you remembering to re-sync.

If you want Claude to check state instead of doing it yourself, paste the output of `git log --oneline -10`, `git status`, or `git diff` into chat.

## Commit messages: use a file, not `-m`

Commit messages often quote literal UI text ("2.1 Article & Menu Item", article titles, etc.), which breaks `git commit -m "..."` the moment the message contains a double quote. Rather than juggling quote types, Claude writes each commit message to `Tutorials/commit-message.txt` and you commit with:

```
git commit -F "Tutorials/commit-message.txt"
```

No escaping, no picking single vs. double quotes — the file's contents become the commit message exactly as written. This file gets overwritten each time there's a new commit ready; once you've committed, its old contents are safely preserved in git history, so there's nothing to clean up.

## Git command cheat sheet

Run these from inside the `JoomlaDocumentation` folder (or any subfolder — git finds the repo root automatically).

| What you want to do | Command |
|---|---|
| See what's changed since the last commit | `git status` |
| See the actual line-by-line changes | `git diff` |
| Stage a specific file | `git add "Tutorials/CM3 WYSIWYG Editor.html"` |
| Stage everything that changed | `git add -A` |
| Commit staged changes with a message | `git commit -m "Your message here"` |
| Send commits to GitHub | `git push` |
| Get the latest from GitHub (e.g. on another machine) | `git pull` |
| See recent history | `git log --oneline -10` |
| See what changed in one commit | `git show <commit-hash>` |

## Future upgrade option

Right now Claude can't see the `.git` folder because only `Tutorials` is shared, not its parent `JoomlaDocumentation`. If it's ever worth it, sharing `JoomlaDocumentation` instead would let Claude run `git log`/`git diff`/`git commit` directly, removing the manual handoff. Not necessary today — just an option if this workflow starts feeling like friction.

## Reference vs. tutorial files

Two files in this folder are themselves published Joomla articles, not just working notes, and should be synced the same way as tutorials if they're edited: `Tutorial Style Guide.html` and `Documentation Glossary of Terms.html`.

`Editing Notes and Open Items.md` and `Tutorial URL Reference.xlsx` are working documents for this project only — they don't correspond to anything in Joomla and don't need to be pasted anywhere. Still worth committing to git for their own history, just not part of the Joomla sync loop.
