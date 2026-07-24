# Editing Notes and Open Items

Working notes for the Joomla tutorial editing project. Not a tutorial article — just state to pick up from if a session is lost.

## Workflow

Tutorials were written by different people over a long period with little shared guidance, so they're inconsistent. We're restructuring/rewriting each one to match the Tutorial Style Guide and Documentation Glossary of Terms (both in this folder). Some style rules weren't defined yet when we started — we're defining and refining them as we go, tutorial by tutorial, discussing each inconsistency before applying it. Jeff can also be inconsistent, so part of my job is catching that and flagging it for discussion rather than silently "fixing" it.

**Before starting a new tutorial**, ask Jeff for its formal title (e.g., "CM10.1 Submenus") to use as the filename, for consistency with his other editors.

## Completed

- Tutorial Style Guide.html and Documentation Glossary of Terms.html re-saved (had been lost when a session died).
- CM10.1 Submenus.html fully edited: Steps/Substeps structure corrected, h4s removed and flattened into a numbered sequence, "View the Results" section rebuilt with Result:/Note: labeling and the glossary's "View the site" shorthand, standalone Summary heading removed (folded into closing paragraph), Setup sections converted from `<ul>` to `<ol>`, "Login" corrected to "Log in," Collie/Collies made consistent (Collies), and step-specific screenshots moved inside their `<li>`.
- Style guide updated with a new rule: in form-field bullets, bold the field name and italicize the literal value (even if it's a full sentence); leave plain text when it's guidance about what to enter rather than a literal value (e.g., "leave blank," or a link to placeholder/lorem ipsum text) — nothing on screen to match against in that case.

## Open questions

1. **Section-summary screenshots**: `article_list.png`, `menu_items_list.png`, and `site_modules_list.png` in CM10.1 Submenus each summarize a completed list of items rather than illustrating one specific step. They're currently left as trailing figures after their list, not nested inside a `<li>`, unlike the step-specific screenshots we moved inline. Never explicitly decided whether this is the right distinction or whether the style guide should say so.

## CM10.4 Adding a New Menu

Mostly edited: stripped copy-paste junk (data-start/end attributes, entity spans, dir="auto", curly quotes), consolidated three h2 "Steps for..." headings into one h2 Steps with four h3 substeps (Create the Menu, Display the Menu with a Site Module, Create an Article, Create a Menu Item — the last two replace the nested `<ol><ol>` structure), fixed Concepts from h3 to h2, applied Login→Log in, Save and close→**Save & Close**, breadcrumb `>` bolding, Result:/Note: labels, and the Click New→nested field-bullet pattern throughout. Fixed the mislabeled screenshot: the first figure (captioned "Creating the new menu") is now creating_the_menu.png at 1944×1140 per Jeff, instead of the duplicate adding_menu_item.png reference. Also fixed CM10.1's "Create a Menu" section to match the same nested field-bullet pattern (it had been left flat/un-nested from an earlier pass).

Resolved:
- Dropping the redundant "Menu: Pets" field bullet was confirmed correct by Jeff — the New Menu Item form does have a Menu selector that lets you reassign the item to a different menu than the one you navigated into, but it's not needed for this tutorial's flow, so leaving it out was the right call.
- Prerequisites bullet "9.2 Menu Modules" now linked as "9.2 Menu Item Modules" → https://guide.joomla.org/modules-positions-menus/9-2-menu-item-modules

CM10.4 has no remaining open items — fully edited.

## CM11.1 Content Tags

Full rewrite drafted, awaiting Jeff's review (he asked to look at it "tomorrow" — not yet confirmed/approved). Original content was thin and structurally broken (an image wrapped in an `<h2>` tag, two stray h2 sections after Steps that didn't fit the standard structure, no real walkthrough for the "Tagged Items" menu item). Rebuilt per Jeff's outline: Setup now creates two tags (Cargo, Insurance) and three articles (one per tag, one with both), reusing the intro paragraph's own Cargo example rather than inventing an unrelated topic. Steps now has three h3 substeps: Create a Tag Menu Item (Cargo only, view frontend), Modify the Tag Menu Item (add Insurance, view frontend again), Filter Articles by Tag in the Backend. The old "Managing Tags" description became the Concepts section. All three original screenshots (taginarticle.png, tag2.png, filter.png) were kept and re-homed into their relevant steps, now properly wrapped in figure/figcaption (they weren't before). Applied all standard rules (Log in, bold breadcrumbs, field-bullet pattern, Result:/Note: labels, Prerequisites list format, View the site / switch to frontend-backend wording).

Reviewed by Jeff on a live site — confirmed working, with corrections applied: Menu Item Type is "Tags &gt; Tagged Items" (nested submenu, not just "Tagged Items"); the field is named "Tag" (singular), not "Tags", on the Tagged Items menu item form; the article Tags field note now says "Select from the dropdown or type..."; and the backend filter step was split in two — Click **Filter Options** (Result: dropdowns appear), then a separate step setting the **- Select Tag -** dropdown to Insurance (the button is "Filter Options," not "Search Tools" as I'd guessed). CM11.1 has no remaining open items.

## Pending / blocked

- **"Article URLs" tutorial**: Jeff pasted this content early in the session thinking it was the Style Guide (it had overwritten the real style guide document in Joomla). Not saved anywhere yet — Jeff is checking Joomla's version history for the correct/most recent version before we do anything with it.
- **CM10.2 Split Menus**: raw content saved as-is (unedited) to CM10.2 Split Menus.html. Jeff says it needs more content work before we start style editing — paused, not reviewed for style compliance yet.
- **CM10.3 Article Display Options Hierarchy**: in progress. Resolved so far: Setup sections converted `<ul>`→`<ol>`; "Save and Close"/"Save and close" standardized to bold **Save & Close**; missing bold added to Content > Categories / New button in Create a New Category and Create Two Articles; Create a Menu Item's wrongly-italicized clickable elements (Menus, Main Menu, New, Options) fixed to bold, plus its field bullets brought in line with the field-name/value rule; Create Two Articles restructured so Title/Category/Options-tab observation nest under the "click New" step with a Result: label, matching the established pattern; the "Author" ambiguity resolved (see style guide — bold only when naming the field itself, no emphasis when referring to who wrote the article) and applied.
  Resolved: second article now created via Click Save & New + repeated field bullets (Olympus Solar Calculator), matching the Add Menu Items repeat pattern from CM10.1, ending in Save & Close. Menu item section renamed "Create a Category Blog Menu Item" with literal values (Sundial Software Blog, Sundial Software) filled in.
  Resolved: the whole Steps section restructured. h4 is now settled for good — never used; distinct demonstrations become sibling h3 substeps instead (applied here: "Demonstrate Global Inheritance" — renamed from "The Global Setting" for parallelism with the other three headings — "Override the Global Setting," "Override the Menu Setting," "Inherit from the Article"). Blockquote asides converted to the existing Note: convention. All narrated paragraphs converted to `<ol>` + Result:/Note: labels. Generic "the category blog menu item" references replaced with the literal menu item name, Sundial Software Blog (bold, since it's clicked both on the frontend and in the backend menu items list). "Close the tab, return to the Admin area" replaced with "Switch to the backend" / "Switch to the frontend" (no "tab") per the glossary's two-tab pattern — first entry to the frontend in a substep still uses "View the site," subsequent returns use "Switch to the frontend." Also fixed a typo, "Contents > Articles" → "Content > Articles".
  Resolved: intro concept screenshots — kept the list-view screenshot, removed the individual-article one (redundant, same concept). Style guide updated with a new rule covering this "concept screenshot in the opening paragraph" pattern, distinct from step-assisting screenshots.
  CM10.3 has no remaining open items — fully edited.

## Prerequisites — resolved

Always an unordered list, always begins with the link to 1 Tutorial Introduction (that tutorial covers site type, frontend/backend login, viewing the site, and switching tabs, so no need to restate). Additional bullets can reference other required tutorials in the same format, or state other tutorial-specific requirements. Style guide updated; applied to CM10.1 and CM10.3 (CM10.3's second bullet about the Main Menu/featured homepage was removed — a fresh Joomla install has these by default, and the Tutorial Introduction is meant to instruct the user to start from a fresh install, so this is already covered). CM10.2 not touched yet (still paused, needs content work first).

Note for whenever "1 Tutorial Introduction" itself gets written/reviewed: it needs to instruct the user to use a fresh Joomla installation (which by default has a Main Menu and a featured-item homepage), plus site type, frontend/backend login, viewing the site, and switching tabs.

## General pattern emerging

Some issues are now showing up across multiple tutorials (Setup using `<ul>` instead of `<ol>`, Prerequisites formatting, h4 usage) — worth treating these as settled style guide rules soon rather than re-litigating per tutorial.
