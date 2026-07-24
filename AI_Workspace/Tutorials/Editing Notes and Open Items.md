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

## CM12.1 Article Metadata

Fully edited. Introduced a new three-tab pattern for this tutorial (backend / frontend / page source, since it's the only tutorial so far that needs to inspect page source alongside the usual frontend/backend switching) — "Switch to the backend," "Switch to the frontend," "Switch to the page source," extending the glossary's two-tab convention. Applied all standard fixes: Prerequisites reformatted as a list (dropped the login sentence, kept the two genuine tutorial-specific requirements — HTML familiarity, ability to view page source); Setup's `<ul>`→`<ol>` with field-bullet nesting; narrated paragraphs in Steps converted to `<ol>` + Result:/Note: labels; "metadata > description area" became the actual Joomla field name, **Meta Description** (unverified against a live site, like a couple of items in CM11.1 — worth double-checking); Robots/Author/Publishing tab formatting fixed to bold-name/italic-value; screenshot moved inside its step; two stray empty `<p>` tags removed from the end.

No open items, pending Jeff's live-site check of the Meta Description field name.

## CM9.1 Custom Module

Full rewrite from reference-doc style into the tutorial structure, drafted and applied (not yet reviewed by Jeff on a live site). Original was organized as exhaustive field-by-field reference documentation rather than a task walkthrough. Rebuilt as: Steps with four h3 substeps (Create the Module, Configure Basic Settings, Set Menu Assignment, Save and View the Result) using the original "Example" section's own concrete values (Sidebar Right, Published, On All Pages, Public, ordered above others); Concepts absorbed the reference material that didn't fit the concrete walkthrough (Status states, Start/Finish Publishing, Ordering behavior, the Note field, the other three Menu Assignment options, and the Options/Advanced/Permissions tabs). Dropped the redundant "two ways to create it" duplication — standardized on Content > Site Modules (matching CM10.1/CM10.4), with a one-line Note mentioning the Home Dashboard alternative instead of a full parallel section.

Update after Jeff's live-site run-through: major revision applied. "Configure Basic Settings" and "Set Menu Assignment" sections removed — fields folded directly into Create the Module's "Click Custom" step as nested bullets (Title, Module Content with sub-bullets for text + image, Position only — Show Title/Status/Access dropped since defaults cover them, Menu Assignment dropped entirely, relying on default). Module Content now has concrete instructions (add text "This site is powered by Joomla," insert powered_by.png via Content > Media) instead of generic guidance. Position value corrected to lowercase "sidebar-right" (real Joomla value, not "Sidebar Right"). "Save and View the Result" section folded into Create the Module as its final two steps. New h3 "Change the Module Order" added — turns out reordering isn't done via the Ordering field on the module form (which Jeff found doesn't actually let you set it) but via a separate filter-and-drag-handle workflow on the Site Modules list screen. Not yet decided whether the old Ordering field even does anything — Jeff said "I'm not sure what this control actually does so let's just leave it."

Resolved: screenshots added (module_sidebar_right.png in Create the Module, ordering.png — an annotated 4-step screenshot — in Change the Module Order); Concepts rewritten to drop the now-inaccurate Ordering-field description entirely, replaced with a bulleted Status/Start-Finish Publishing list, condensed Menu Assignment/Permissions mentions, and a closing note about other module types. Note: this pasted version was a redo — Jeff lost the first round of these edits and had to redo them from scratch.

Resolved:
- Dynamic content (YouTube embed, weather/stock ticker) dropped for good — other module types already cover some of this, and Jeff didn't want to compound the complexity the reordering section already added.
- Concepts' bulleted Status/Publishing list converted back to prose, keeping it consistent with every other Concepts section across all tutorials.
- Standardized on "drag handle" (Joomla's own codebase calls this the sortable-handler / icon-menu, three vertical dots; "drag handle" is the term used in Joomla community docs/forums). Step text updated from "gray dots" to "drag handle (three dots)" on first mention, then "drag handle" thereafter. Also added to the glossary (text-only for now; Jeff may add a screenshot to that glossary entry later). Figcaption still says "three dots" — fine as a visual description, no change needed.
- Both new images were missing `class="float-none"` (present on every other image across all tutorials) and the closing `<br><br>` before `</li>` — added both back in silently as a mechanical fix.

Resolved: Options/Advanced tab descriptions left out of Concepts for good — Jeff decided the tutorials shouldn't delve too deeply into advanced options.

CM9.1 has no remaining open items — fully edited.

## CM10.2 Split Menus

Rewritten from generic reference-style guidance into a concrete tutorial (original was more "how to do this on your own site" than a walkthrough with real content, similar to the problem CM9.1 and CM11.1 had). Designed a concrete two-level scenario: two top-level items (Coffee, Tea), each with two children (Espresso/Latte under Coffee; Green Tea/Black Tea under Tea) — six articles total, each with real (not placeholder) content specific to its name, so the split-menu behavior is visibly obvious when clicking through.

Structure: Setup creates the six articles; Steps has four h3 substeps — Create a Multi-Level Menu (six menu items, Single Article type, parented appropriately), Configure the Top-Level Menu Module (Start/End Level 1, Show Submenu Items No), Configure the Secondary Submenu Module (Base Item: Current, Start Level 2, End Level All, Show Submenu Items Yes), and View the Results (click Coffee → sidebar shows Espresso/Latte; click Tea → sidebar updates to Green Tea/Black Tea, demonstrating the dynamic behavior that's the actual point of a split menu). Concepts explains the Start/End Level mechanism, Base Item: Current, and mentions Menu Assignment as a way to scope the secondary module away from pages like the homepage. Kept all three original screenshots, now properly nested inside their relevant steps.

Applied all standard conventions throughout (bold breadcrumbs, field-bullet pattern, Result: labels, Prerequisites list format, Save & New repeat pattern for the six articles/menu items).

Resolved: "menu" confirmed correct for the top-level module's Position by Jeff on a live site.

Live-site corrections applied: field renamed "Show Submenu Items" → "Sub-menu Items" with values Show/Hide (not Yes/No); "submenu" hyphenated to "sub-menu" throughout (module title "Sidebar Sub-menu", both h3 headings, "sidebar sub-menu" in View the Results); headings shortened, "Configure the Top-Level Menu Module" → "Configure the Top Menu", "Configure the Secondary Sub-menu Module" → "Configure the Sub-menu"; Base Item field turned out not to have a literal "Current" option on the live form — changed to "leave blank" (plain text, not italicized, matching the non-literal-value convention), and the Concepts paragraph explaining it updated to match.

Style guide updated: screenshot spacing at the end of a list item changed from "one or two <br> tags" to a single <br> before and after — Jeff found this works best in practice. Applied throughout CM10.2's figures.

Resolved:
- Screenshot placement was intentional — Jeff reshot all the images to accurately reflect the current tutorial content and removed the old ones. Added the real caption, "Configuration of the main menu module," to the first figure (was a placeholder).
- Position field formatting stays inconsistent between CM10.2 ("Sidebar left [sidebar-left]") and CM9.1 ("sidebar-right") on purpose — Jeff doesn't want to standardize these, they're deliberately different per tutorial.

CM10.2 has no remaining open items — fully edited.

## Pending / blocked

- **"Article URLs" tutorial**: Jeff pasted this content early in the session thinking it was the Style Guide (it had overwritten the real style guide document in Joomla). Not saved anywhere yet — Jeff is checking Joomla's version history for the correct/most recent version before we do anything with it.
- **CM10.2 Split Menus**: RESOLVED — moved out of Pending. See dedicated section below.
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
