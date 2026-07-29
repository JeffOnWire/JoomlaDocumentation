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

## Site structure — resolved

The site is organized into numbered sections (Section 1, etc.), each with an overview page linking to all tutorials in that section. CM1 "Tutorial Introduction.html" is the Section 1 overview page, linking to its 3 tutorials: CM1.1 Admin Login, CM1.2 Site Login, CM1.3 Viewing the Site.

Resolved: the `href="1-introduction"` link used across every tutorial's Prerequisites (CM9.1, CM10.1, CM10.2, CM10.3, CM10.4, CM11.1, CM12.1, and the Style Guide's own example) was already pointing to the right place — it turned out to be a correct guess, not a placeholder. Per Jeff: prerequisites in sections 2–12 should always point to the Tutorial Introduction page, which itself is meant to signal that everything on it — including 1.1, 1.2, and 1.3 — is a required prerequisite. Updated the description text on that link bullet (all 8 files) from "covers where to run your tutorial and administrative access" to "covers where to run your tutorial, and includes the required frontend/backend login and site-viewing tutorials (1.1, 1.2, 1.3)" to make that explicit.

CM1.3's Prerequisites is the exception, by design — it's part of Section 1 itself, so it links directly to CM1.1 and CM1.2 (its actual specific prerequisites) rather than to the CM1 overview.

CM1, CM1.1, CM1.2, CM1.3 are now fully edited:
- CM1: login→log in fix, link list converted from padded paragraph to proper `<ul>`, trailing empty `<p>` removed, "behaviors"→"behaviours" (see British spelling below).
- CM1.1: Prerequisites as `<ul>`, Log In/Log Out/User Menu/Toggle Menu bolded, Result: labels added, screenshot spacing fixed to single `<br>`, login/log in verb fixed. Image mismatch resolved — Jeff confirmed login-screen_2.png is correct; resized to 960×539 (proportional) to match the site convention. "Explore the Layout" rewritten from descriptive paragraphs into directive numbered steps (Toggle Menu, expand a menu heading, select a submenu item, note the header) per Jeff's request. Concepts replaced with Jeff's own three-paragraph version (administrative area/permissions/frontend-backend login distinction), with "login"→"log in" verb fix applied.
- CM1.2: Prerequisites as `<ul>`, Log In/Log Out bolded, Result: label folded in, typo fix ("users. controls"→"users, controls"), Log In/Log Out capitalization fixed in figcaption, login/log in verb fixed, Concepts to prose.
- CM1.3: Result: label colon-placement fix.

No remaining open items for CM1/CM1.1/CM1.2/CM1.3.

## British spelling — resolved

Jeff confirmed: use British spelling throughout (Joomla platform and its docs use British spelling). Added to the Style Guide. Full sweep done across all edited files for stray American spellings (-ize/-or endings): "behaviors"→"behaviours" (CM1), "minimizes"→"minimises" (CM1.1), "organized"→"organised" (CM10.1), "customizable"→"customisable" and "flavor"→"flavour" ×3 (CM10.2), "individualize"→"individualise" (CM10.3), "recognize"→"recognise" and "italicize"→"italicise" (Style Guide), "standardized"→"standardised" and "recognizable"→"recognisable" (Glossary). No remaining American spellings found.

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

## Section 2 (CM2, CM2.1–CM2.5)

Jeff saved the section 2 overview page (CM2 "First Steps.html") and its 5 tutorials for editing.

Resolved: CM2's original content was a copy/paste error (it had CM1.3's frontend/backend-switching content) — Jeff replaced it with the real section 2 overview, a link list to 2.1–2.5 using `index.php?Itemid=NNN` hrefs.

Resolved: CM2.4's "In the Administrator Menu, expand Content and click on Menus > Menu Items" was wrong navigation (Content and Menus are separate top-level admin items) — Jeff confirmed, "expand Content and" removed.

Resolved: CM2.5's Concepts section (about the Page Display tab / Show Page Heading field) didn't match the tutorial's actual topic (the Save to Menu shortcut) — likely leftover/misplaced content. Removed entirely per Jeff; he's filing an issue to come back and write real Concepts content for this tutorial once he's reviewed the article.

Resolved: Jeff provided the real published URLs for CM2 and CM2.1–2.5. Fixed all `index.php?Itemid=NNN` links in CM2 (overview list) and CM2.5 (intro paragraph, Prerequisites, "Save to Menu for Categories") to the real slugs, all under `content-management-first-steps/`: 2.1 `create-an-article-and-menu-item`, 2.2 `category`, 2.3 `category-menu-item`, 2.4 `featured-articles`, 2.5 `save-to-menu`. Standardized the link text used everywhere a tutorial references these siblings to "2.1 Article & Menu Item" / "2.2 Creating a Category" / "2.3 Category Menu Item" (previously worded inconsistently between CM2, CM2.3, and CM2.5).

Checked section 1's own `href="1-introduction"` link against the real URL Jeff uses — it was already correct (no fix needed there). Section 1 uses a numbered slug while section 2 uses a descriptive one; Jeff is looking into why that's inconsistent on the live site, separately from this editing pass.

Full mechanical style pass done across CM2/CM2.1–2.5: Concepts converted to prose throughout; Result:/Note: labels added inline (CM2.3 previously used a different pattern — nested `<ul>` bullets describing outcomes instead of inline Result: labels — standardized to match every other tutorial); bold/italic field-value convention applied (field name bold, literal value italic); breadcrumb bolding consolidated (e.g. "expand X and click Y" → "click X > Y"); screenshot spacing fixed to single `<br>` before/after; CM2.5's bare `<img>` tags (no figure/figcaption, unlike every other tutorial) wrapped properly; British spelling applied (organizes→organises, characterized→characterised, etc.); "tap"→"click" standardized (CM2.5 had touch-device wording, inconsistent with the rest of the corpus); "menu-item"→"menu item" (no hyphen) standardized; various HTML cleanup (broken/overlapping `<strong>` tags in CM2.4, garbled nested `<em>` tags in CM2.5's "Save to Menu a</em><em>s</em> Blog", stray non-breaking spaces, a bolded-empty-space artifact in CM2.2, missing alt text, CM2.3's "Creating a Category List Layout" h2 fixed to h3 for parallelism with its sibling heading).

CM2/CM2.1–2.5 have no remaining open items, aside from Jeff's planned follow-up to write real Concepts content for CM2.5 (see above).

## Section 3 (CM3, CM3.1–CM3.5)

Jeff sent real URLs for CM3 and CM3.1–3.5 (all under `wysiwyg-editor/`). While confirming CM1.3's URL, discovered it needed a numbered prefix Jeff hadn't mentioned before: `1-introduction/1-3-viewing-the-site`, not the `1-introduction/viewing-the-site` guess used in CM1's overview — fixed. CM1.1 and CM1.2 were re-confirmed as already correct (`1-introduction/admin-login`, `1-introduction/site-login`), no fix needed.

Built `Tutorial URL Reference.xlsx` in the Tutorials folder — a running reference of every tutorial's filename and href/URL, color-coded Confirmed (green) / Guessed-unconfirmed (yellow) / Not started (gray), so Jeff can fill in real URLs in one pass instead of one-at-a-time chat questions. While building it, discovered section 4 (CM4 Images, CM4.1–4.3) and section 5 (CM5 Delete/Archive/Filter, CM5.1–5.3) already exist as draft files in the folder, untouched — logged in the spreadsheet, not edited yet.

CM3.3 Lists has no Concepts section (only tutorial so far without one) — Jeff confirmed leave it out for now rather than draft one.

Full mechanical style pass done across CM3/CM3.1–3.5: real links applied throughout; Concepts converted to prose (except CM3.3, left without one per Jeff); Result:/Note: labels added inline, replacing nested "what happened" bullets in CM3.4 and CM3.5; bold/italic convention applied (systematic italic-for-clickable-elements issue across CM3.2/3.4/3.5 fixed to bold); breadcrumb bolding consolidated, including CM3.3's literal "->" arrow (explicitly disallowed by the style guide) replaced with a bold breadcrumb; "tap"→"press" for keyboard keys (Return, Tab, Escape) and "tap"→"click" for buttons/icons, matching the CM2.5 tap→click precedent; CM3.3's bare `<img>` tags (no figure/figcaption, same issue CM2.5 had) wrapped properly, and missing `class="float-none"` added; British spelling applied (organized→organised, customizations→customisations, emphasize→emphasise, etc.); CM3.4/CM3.5's Prerequisites (previously a bare paragraph before the list, and CM3.4 listing 1.1/1.3 individually) restructured to the standard single Tutorial-Introduction-link format, per Jeff's section 2–12 rule; CM3.5's stray "Tables" h2 (redundant mid-document heading) merged into the opening paragraph; various typo/grammar cleanup (stray "C" character in CM3.1, "1.0 Admin Login"→dropped in favor of the standard intro link, sentence fragments in CM3 and CM3.2's intros, period-inside-em artifacts).

CM3/CM3.1–3.5 have no remaining open items.

## Sections 4–12: all files now in the folder

Jeff added every remaining tutorial file to the Tutorials folder (sections 4–12 complete) and partially filled in the URL Reference spreadsheet's Notes column (confirmed real URLs for sections 4 and 5, and CM6's overview).

Rebuilt `Tutorial URL Reference.xlsx` with every tutorial now present, keeping Jeff's confirmed entries. While researching hrefs, found that several section overview pages (CM6, CM7, CM8, CM9, CM10, CM11, CM12) already contain real-looking slugs in their own sub-tutorial link lists — not Itemid placeholders. Added a new "Found in file" status (distinct blue color) for these, separate from "Confirmed" (Jeff-verified) and "Guess" (no source at all), since they look reliable but haven't been checked against the live site.

Flagged a few things worth Jeff's attention in the spreadsheet Notes, not yet acted on:
- CM7's overview page only lists 7.1–7.4; it's missing 7.5 (Locking an Article) and 7.6 (Edit Permissions for Articles) entirely — likely an outdated overview page.
- A few title mismatches between overview link text and actual filenames: CM7.4 ("View Access Restrictions" vs. filename "Restrict Access to Articles"), CM8.2 ("Article URLs" vs. filename "Different URLs for Content"), CM9.1 (overview has a typo, "Cutom Module", and its slug says "adding-text" rather than anything matching "custom-module").
- CM9.2's found slug (`modules-positions-menus/9-2-menu-item-modules`) matches the link already used in CM10.4's Prerequisites, which was confirmed correct earlier — good cross-check.

Have not started editing sections 4–12's content yet — that's pending, section by section, same as 2 and 3.

## URL reference: fully confirmed

Jeff filled in every remaining row of `Tutorial URL Reference.xlsx` by pasting raw URLs into a new column H ("Raw URL"), rather than typing into the Notes column — a good approach, keeps the two separate. Every tutorial through section 12 is now Status: Confirmed.

Applied the confirmed URLs to fix every remaining broken link found site-wide (grepped for `index.php?Itemid=` and `Itemid=` across all files — zero left): CM4's overview list (4.1/4.2/4.3, previously Itemid placeholders); CM5's overview list (5.1/5.2/5.3, same); CM4.3's Prerequisites reference to "2.1 Article & Menu Item" (was Itemid=469); CM10.4's Prerequisites reference to "2.0 First steps with articles, menu-items and categories" (was Itemid=468, also cleaned the odd "2.0" numbering and wording to "2 First Steps" to match the real tutorial's title).

Confirmed via Jeff's URLs: CM9.1's existing guess for "4.1 Images in Articles" and CM10.4's existing guess for "9.2 Menu Item Modules" were both already correct — no changes needed there.

Resolved: CM7's overview page was missing 7.5 and 7.6 — added both, using their confirmed URLs and short descriptions drawn from each tutorial's own opening paragraph. Updated the spreadsheet Notes accordingly.

Resolved: CM7.4/CM8.2/CM9.1 overview link text mismatches. Jeff confirmed the filenames are the correct titles, not the overview text — updated CM7's "7.4 View Access Restrictions"→"7.4 Restrict Access to Articles", CM8's "8.2 Article URLs"→"8.2 Different URLs for Content", and fixed CM9's "9.1 Cutom Module" typo→"9.1 Custom Module". Spreadsheet Notes updated to match.

Sections 4–12 have no remaining known link/title issues. Still pending: the actual mechanical style pass on sections 4–12's content, section by section, same as 2 and 3.

## Section 4 (CM4, CM4.1–CM4.3)

Full mechanical style pass done across all four files: real links already in place from the earlier URL work; Concepts converted to prose (CM4.3 has no Concepts section, consistent with the CM3.3 precedent — not flagged again, just followed it); bold/italic convention applied throughout (CM4.2 and CM4.3 both had systematic italic-for-clickable issues); Result:/Note: labels added inline; breadcrumb bolding; CM4.2's Prerequisites bare `<img>` tags given alt text and cleaned up; CM4.3's bare `<img>` tags wrapped in proper figure/figcaption (same gap CM2.5 and CM3.3 had); British spelling; invalid HTML fixed (a `<ul>` sitting as a direct sibling of `<li>` inside an `<ol>` in CM4.2 — not valid, folded into the preceding `<li>`); malformed nested `<em>` tags spanning images fixed in CM4.3; several small typos (stray unmatched parenthesis, "screens"→"screen", "This the image"→"This is the image", "For this our upcoming article"→"For our upcoming article"); CM3.3-style ASCII arrow ("Content -&gt; Articles") fixed to bold breadcrumb in CM4.3; h3 headings in CM4.3 changed from sentence case to Title Case for consistency with sibling headings elsewhere.

Resolved: CM4.1's Attribution listed three image credits (Crab Nebula, Jupiter, Andromeda Galaxy) though the tutorial only visibly uses one (Crab Nebula), and the Jupiter credit's link pointed to the Crab Nebula URL (copy-paste error). Jeff confirmed all three stay — the extra two images appear in a screenshot, not as tutorial content — and provided the correct Jupiter URL (https://commons.wikimedia.org/wiki/File:Jupiter_rendered_with_Blender.webp), now applied. Also fixed two unrelated attribution typos while in there: "Napoleon II Telescope" → "Napoleon III Telescope" and "Equitorial" → "Equatorial" in CM4.2 (both clear typos against the image's own filename).

Resolved: Jeff confirmed no Troubleshooting section exists or is planned — both "check the Troubleshooting paragraph" references removed from CM4.3.

Section 4 (CM4, CM4.1–4.3) has no remaining open items.

## Section 5 (CM5, CM5.1–CM5.3)

Full mechanical style pass done across all four files. No blocking questions this time — everything was either an established rule or an unambiguous fix. Applied: Concepts converted to prose; Result:/Note: labels added inline (replacing bare "what happens" sentences and nested nested-bullet nesting); bold/italic convention applied; breadcrumb bolding; screenshot spacing to single `<br>`; curly quotes (copy-paste artifacts) straightened; stray empty `<em>` tags wrapping whitespace/images removed; unnecessary inline `style="font-size: 1rem;"` spans stripped; standardized the "2.1 Article & Menu Item" prerequisite link text to match the shorthand used everywhere else (these three files all had the longer "2.1 Creating an Article and Menu Item" instead); British spelling.

Fixed: "Troubador" (used inconsistently, 4 times) standardized to the correct spelling "Troubadour" throughout CM5.2, matching the one place it was spelled correctly (the Setup section's Title field). Typos: "buttton"→"button", "cateogries"→"categories", "archive"→"archived" (CM5.3), missing "d"/words in a couple of sentences.

Structural fix: CM5.3 had two full Steps-type h3 subsections ("Archiving an Article from the Articles List" and "Archiving via a Menu Item") sitting after the Concepts section — moved them back into Steps, before Concepts, matching every other tutorial's Prerequisites → Steps → Concepts → Attribution ordering.

Section 5 has no remaining open items.

## General pattern emerging

Some issues are now showing up across multiple tutorials (Setup using `<ul>` instead of `<ol>`, Prerequisites formatting, h4 usage) — worth treating these as settled style guide rules soon rather than re-litigating per tutorial.

## Section 6 (CM6, CM6.1–CM6.2)

Full mechanical style pass done across all three files. URLs were already confirmed (Tutorial URL Reference.xlsx) and needed no changes. No blocking questions — all fixes were established rules or unambiguous.

CM6 overview: converted the link list from a `<p style="padding-left:40px;">` with `<br>`-separated links into a proper `<ul>`, matching every other overview page; added "6.1"/"6.2" numbering to the link text to match the numbering convention used elsewhere.

CM6.1: Setup sections converted from `<ul>` to `<ol>` (steps convention); fixed invalid nesting where a `<ul>` sat as a sibling of `<li>` instead of inside it; removed a duplicated/dangling "Return to the Home Dashboard" step that didn't match the actual flow (was missing the "Click New" step entirely — added it); converted breadcrumb-style navigation ("expand Content and click on Articles") to the bold `Content > Articles` format; fixed field-list bold/italic direction throughout (field name should be bold, value italic — was reversed); added Result: labels; fixed "and and" duplicated-word typo in the opening paragraph; realigned the "Note the following features" list in the View the Article section so its five items correspond one-to-one with the five numbered callouts in that section's own screenshot caption (previously mismatched — item 1 in the text didn't match callout 1 in the image); moved the two page-break screenshots into the step they illustrate, per the screenshot-placement rule; converted the "Modify the Page Breaks" prose into numbered steps; removed a trailing empty paragraph.

CM6.2: removed leftover `dir="auto"` attributes (copy-paste artifacts) throughout; standardized "2.1 Articles & Menu Item" → "2.1 Article & Menu Item" to match the shorthand used everywhere else; Setup sections' field lists fixed to bold-name/italic-value convention (was reversed, and one sub-list used `<ol>` instead of `<ul>`); breadcrumb bolding applied to "Content > Articles" and "Menus > Main Menu"; removed a stray underline span on "New" in "Save & New"; added Result:/Note: labels throughout Steps; collapsed doubled `<br><br>` before screenshot groups to the single-`<br>` convention; added the missing `class="float-none"` to all `<img>` tags for consistency with every other file; Concepts section converted from a bulleted list to prose paragraphs, matching the pattern used since Section 4/5.

Section 6 has no remaining open items.

## Section 7 (CM7, CM7.1–7.6)

Full mechanical style pass done across all seven files. URLs were already confirmed and needed no changes.

CM7 overview: converted from the `<p style="padding-left:40px;">`/`<br>` layout to a standard `<ul>`, matching every other overview page (link text already had 7.x numbering, so no change needed there).

Two open questions resolved by Jeff:
- CM7.1's opening paragraph is literally the placeholder text "Intro text ... t.b.d." — never written. Jeff has logged this as a separate issue for future work; left untouched here, still needs real content.
- CM7.3 (Timed Publishing) had a 4th intro paragraph (the "picture frames" analogy about menu items/articles/categories) that was word-for-word identical to CM7.2's own intro and unrelated to Timed Publishing — clearly an accidental copy-paste. Removed per Jeff's confirmation.

Across all six sub-tutorials: bold/italic field-list convention fixed everywhere it was reversed (field name should be bold, value italic — this was the single most common bug in this section); Result:/Note: labels added throughout, replacing bare "what happens next" sentences; arrow-based breadcrumbs (→) replaced with the bold `>` format in CM7.4; underline `<span>` styling removed (CM7.2, CM7.4, CM7.6); Concepts sections converted to prose where still bulleted (CM7.1); British spelling fixes, most notably "Unauthorized" → "Unauthorised" standardized throughout CM7.4 (was inconsistent — half the file already had it right) and "Uncategorized" → "Uncategorised" in CM7.6.

Structural/content fixes: CM7.1 had a genuinely broken Prerequisites link (escaped HTML tags rendering as literal text, plus a "contnet" typo) — replaced with the standard `<a href="content-management-first-steps">2 First Steps</a>` format used elsewhere; CM7.1 also had "Olympus Solar Companion" where every other reference in the file said "Olympus Solar Calculator" (typo, fixed); CM7.1 had a malformed `<li>` missing a closing `</strong>` tag. CM7.2 referenced "History Blog" (a menu item) where the sentence was actually about unpublishing the second *article*, which is "Medieval Europe" — fixed. CM7.4 had two bare `<img>` tags with non-descriptive alt text ("Step 3 screenshot", "Step 5 screenshot", "Step 6 screenshot") — wrapped in proper figure/figcaption with descriptive captions, matching the CM2.5/CM3.3/CM4.3 precedent (image dimensions left unset where not previously known, rather than inventing values). CM7.6 was missing its `<h2>Setup</h2>` heading entirely — added; CM7.6's Setup sections also had flat, un-nested field lists ("Title: Article List" as bare list items with no field/value distinction) — restructured into the standard nested-list field format. CM7.5's Setup list converted from `<ul>` to `<ol>` (steps convention).

Section 7 has one remaining open item: CM7.1's placeholder intro paragraph, tracked separately by Jeff.

**Resolved:** Jeff supplied real intro text for CM7.1: "In this tutorial we will demonstrate that both an article and its category must be published for the article to appear on the website." (tweaked "a website" → "the website" to match house usage). Applied. Section 7 now has no remaining open items, and the whole project (sections 1–12) has no known open items.

## CM5.1 content redesign (post-completion revision)

Jeff requested a content redesign of CM5.1, not a style pass — replacing the Author filter with a Featured filter, and adding a real Setup section (previously this tutorial relied on default Joomla sample content — Typography/Blog/Help categories, Joomla Tester/Joombassador authors — rather than creating its own).

New Setup creates two categories (<em>News</em>, <em>Events</em>) and eight articles — one for every combination of category × featured × published status (a full 2×2×2 matrix): New Product Launch (News/Featured/Published), Upcoming Announcement (News/Featured/Unpublished), Company Update (News/Unfeatured/Published), Draft Press Release (News/Unfeatured/Unpublished), Annual Conference (Events/Featured/Published), Conference Preview (Events/Featured/Unpublished), Local Meetup (Events/Unfeatured/Published), Meetup Planning Notes (Events/Unfeatured/Unpublished).

This matrix makes each filter step return a mixed, predictable result per Jeff's spec: filtering on Status=Unpublished returns all four combinations of category/featured; filtering on Category=News returns all four combinations of featured/published; the final combined filter (Status=Published, Category=News, Featured=Featured) narrows to exactly one article (New Product Launch), demonstrating how combined filters narrow rather than broaden.

Steps restructured: "Navigate to the Articles List" unchanged; "Filtering on Article Status" and "Filtering on Category" keep their original flow/mechanics but now reference the new categories/articles; "Filtering on Status, Category and Author" renamed to "Filtering on Status, Category, and Featured" and redesigned around the new combined-filter demonstration.

**Open items needing Jeff's live-site verification (same pattern as CM9.1/CM10.2/CM11.1's initial drafts):**
- The Featured filter dropdown is guessed as **- Select Featured -** with values <em>Featured</em>/<em>Unfeatured</em>, matching the naming pattern of the other filter dropdowns (**- Select Status -**, **- Select Category -**). Not yet confirmed against a live install.
- All eight figures in this file are unchanged from the old version and still reference the old sample content (Typography, Blog, Help, authors) visually, even though captions/alt text have been updated to describe the new content. These screenshots need to be retaken once the new Setup content exists on a live site — same process used for CM10.2's reshoot.

**Planned follow-up:** this same News/Events category pair and eight-article set is meant to carry into CM5.2 (Delete Articles) and CM5.3 (Archive Articles), with their own Setup sections referencing or extending this content as needed, once CM5.1 is confirmed working. Not started yet.

**Round 2 revisions (Jeff's detailed feedback), applied:**
- Setup field order for each article changed to Title, Status, Category, Featured, matching the actual on-screen form order.
- Setup headings de-numbered: "Create Two Categories" → "Create Categories", "Create Eight Articles" → "Create Articles" (avoids sounding intimidating). Added a one-line intro under "Create Articles" noting it moves quickly (title + three field selections per article).
- "Filtering on Article Status": dropped "spanning both categories and both featured states" from the Result sentence; replaced the two trailing prose paragraphs with two real steps — step 2 changes the filter to Published, step 3 resets it via "- Select Status -".
- "Filtering on Category": dropped the intro sentence; merged the old separate "Result" steps into the steps that produced them (was 6 list items, now 4), keeping the remove-Events and Clear steps as-is.
- "Filtering on Status, Category, and Featured": step 1's field order changed to Featured, Status, Category to match the real dropdown order on the filter bar (heading/prose order left as Status/Category/Featured — only the literal step matches screen order); added a final step to Clear the filter.
- New substep added, named "Bulk Actions on Filtered Articles": filters on Featured=Featured + Status=Unpublished (narrows to the two articles that match: Upcoming Announcement, Conference Preview), ticks the select-all checkbox, uses the Actions dropdown to publish both, then clears the filter. No screenshots yet — new content, nothing to reuse.
- Confirmed "substep" is already an established term — it's defined in the Tutorial Style Guide itself (h3-level subsections within Steps), not something that needed adding.
- Concepts rebuilt: removed the Articles/Category/Featured-definition paragraphs entirely; kept only the filter paragraph, changing "Multiple filters can be combined" → "Multiple criteria can be combined"; added a new paragraph on filtering as a way to bulk-act on articles (publish/archive multiple at once); added a new paragraph noting similar filter options exist in Categories, Menus, and other content list views.

Confirmed by Jeff: "- Select Featured -" is the real dropdown name (no fix needed). "Bulk Actions on Filtered Articles" confirmed as the substep name.

**Round 4: real screenshots added.** Jeff supplied five screenshots from his live-site run-through, saved to `images/articles/324/`: filter_options.png, unpublished_articles.png, news_and_events_articles.png, published_featured_news_articles.png, bulk_action.png. Read each one directly to get exact pixel dimensions (via PIL) and to verify on-screen content before writing captions/alt text. Placed: filter_options.png after "Filtering on Article Status" step 2 (filter options open); unpublished_articles.png after step 3 (Select Status dropdown + Unpublished + resulting 4-article list, in one shot); news_and_events_articles.png after "Filtering on Category" step 2 (both categories added, all 8 articles); published_featured_news_articles.png after "Filtering on Status, Category, and Featured" step 1 (combined filter narrowing to one article); bulk_action.png after "Bulk Actions on Filtered Articles" step 3 (Actions dropdown, Publish highlighted).

Two corrections surfaced by actually looking at the screenshots against the live site, applied to the file:
- The article Jeff created was titled **Product Launch**, not "New Product Launch" as I'd drafted — fixed everywhere (Setup and the combined-filter step).
- The Featured filter dropdown's actual selected-value label is **Featured Articles**, not just "Featured" — fixed in both places it's used as a literal value (combined-filter step, Bulk Actions step). The dropdown's placeholder name, "- Select Featured -," was already correct.

The live filter bar screenshot also confirms the real on-screen dropdown order top-left-to-right is Featured, Status, Category, Access / Author, Checked Out, Tag, Max Levels — matching the Featured→Status→Category order already applied in round 3.

CM5.1 now has real screenshots throughout and no more open items, aside from the still-pending CM5.2/CM5.3 follow-up (reusing this News/Events content).

**Round 3 revisions, applied:**
- Removed the "for us as authors, not the user" summary paragraph at the end of "Create Articles" (the one explaining the 8-article combination matrix).
- Dropped the "Navigate to the Articles List" substep entirely; folded its two real actions into "Filtering on Article Status" as its new steps 1–2 (Click Content > Articles → list appears; Click Filter Options → filter options appear). Also dropped the login/Home Dashboard step that used to lead that substep — not requested to keep it, and no other substep in this file has one either.
- "Filtering on Category" — last step (Clear) now also states the filter dropdowns disappear, not just that the list refreshes.
- Removed "eight" everywhere it modified "articles" throughout the file — every "Result" now just says "all articles" rather than "all eight articles." (The actual count is still fully specified in Setup, just not repeated as a magic number in Steps.)
- **All figures removed from the file.** Every existing screenshot showed old sample content (Typography/Blog categories, Author names) that no longer matches this tutorial's Setup, so per Jeff's request I'm treating this as a blank slate and proposing a fresh, prioritized screenshot list instead of leaving stale image references in place. See the recommendation list delivered in chat (also worth copying here once finalized): filter bar overview after "Filtering on Article Status" step 2; Select Status dropdown extended + Unpublished highlighted after step 3; category-filter result list after "Filtering on Category" step 2; the three-dropdown combined-filter view + single-article result after "Filtering on Status, Category, and Featured" step 1; header checkbox + Actions dropdown open on Publish in "Bulk Actions on Filtered Articles" step 2/3. None inserted into the HTML yet — waiting on real screenshots from Jeff's live-site run-through, same as every other tutorial's screenshot cycle.

## Section 8 (CM8, CM8.1–8.2)

Full mechanical style pass done across all three files. URLs already confirmed, no changes needed. No blocking questions — this was a relatively clean section; CM8.1 in particular was already close to full compliance (bold/italic, figures, and breadcrumb bolding were already correct — only added one Result: label for consistency).

CM8 overview: converted from padding/br layout to a standard `<ul>`; fixed a duplicated-word typo ("change change"); fixed "how their relation to menu items" grammar; "optimize" → "optimise".

CM8.2: removed a stray underline `<span>` around "will" in the opening paragraph; restructured Setup and Steps field lists from flat "Title: X" bullets into the standard nested bold-name/italic-value format throughout (Create a New Category, Create an Article, Create a Category Blog Menu Item, Single Article Menu Item, Create a Redirect); added Result:/Note: labels; British spelling fixes ("recognized"→"recognised" ×4, "recognizable"→"recognisable", "Search Engine Optimization"→"Search Engine Optimisation").

Section 8 has no remaining open items.

## Section 9 (CM9, CM9.1–9.2)

Full mechanical style pass done across all three files. URLs already confirmed, no changes needed. No blocking questions — the cleanest section yet; CM9.1 was already almost fully compliant.

CM9 overview: converted from padding/br layout to a standard `<ul>`; fixed "Demonstrates modules are used to display menus" grammar to "demonstrates how modules are used...".

CM9.1: only minor fixes needed — added missing `class="float-none"` to two `<img>` tags, and collapsed doubled `<br><br>` around both figures to the single-`<br>` convention.

CM9.2: fixed several field-list values that had bold field names but weren't italicizing the value (Title, Type/Menu Item Type, Position, Module Assignment — appeared four times across the Setup section); changed "click on the Login Form module" to bold (it's the item being clicked, not just referenced) while leaving other Login Form references italic since they're descriptive, not click targets; minor "click on" → "click" tightening on two tab-navigation steps.

Section 9 has no remaining open items.

## Section 10 (CM10, CM10.1–10.4)

Full mechanical style pass done across all five files. URLs already confirmed, no changes needed. No blocking questions — another clean section overall, though CM10.1 needed the most rework of the four sub-tutorials.

CM10 overview: converted from padding/br layout to a standard `<ul>`; removed trailing junk markup (`<p> </p>` and an empty `<pre> </pre>` at the end of the file); fixed "organized"→"organised", "customizable"→"customisable", and a subject-verb agreement error ("The menu for these tutorials are grouped" → "is grouped"); reworded the 10.2 and 10.4 descriptions from imperative ("Learn how to...", "Create a new menu...") to the descriptive style used by every other overview entry.

CM10.1: restructured the "Create the Articles" setup, which had an awkward/redundant flow (entering "Animals" as a title, then a separate "repeat to create all seven articles" step that re-listed Animals) into a single clean repeat-list step; added `class="float-none"` to seven `<img>` tags that were missing it (this file had never gotten that fix); collapsed doubled `<br><br>` to single `<br>` around figures in the "View the Results" section; changed "Click on the Animals menu" to bold (it's clicked, not just referenced).

CM10.2: fixed "oxidized"→"oxidised" (×2); added missing `class="float-none"` to four images. Otherwise already fully compliant — field lists, Result:/Note: labels, and breadcrumb bolding were all correct already.

CM10.3: fixed "viewing and article"→"viewing an article" typo; added missing `class="float-none"`; changed two "Click on X and then Y" navigation phrases to the standard bold `X > Y` breadcrumb format; simplified "click on the New button" to "click New" in two places.

CM10.4: fixed an actual mislabeled cross-reference in the Concepts section — it cited "Tutorial 1.2 Creating an Article and Menu Item" with a link to the section-2 URL, but 1.2 is Site Login; corrected to "2.1 Article & Menu Item" to match the standardized shorthand used everywhere else. Also fixed a Prerequisites link that used a full external URL instead of the internal relative-link format; changed a Home Dashboard reference from italic to bold (it's a UI element, not a value); added missing `class="float-none"` to four images; collapsed doubled `<br><br>` to single `<br>` around three figures.

Section 10 has no remaining open items.

## float-none: reverted, and dropped from style going forward

I had added `class="float-none"` to images throughout Section 10 (and every prior section), treating it as house style since it appeared on most existing images. Jeff clarified this was already decided against previously — the attribute doesn't do anything useful, and standardizing "don't add it" isn't the kind of thing that belongs in the style guide (there could be a future edge case where float-none is actually needed for a specific image). Removed it from all 16 images across CM10/CM10.1–10.4. Going forward: stop adding `float-none` to images. Not going back to re-strip it from sections 1–9 unless Jeff asks.

## Section 11 (CM11, CM11.1)

Full mechanical style pass done across both files (this section has only one sub-tutorial). URL already confirmed, no changes needed. No blocking questions — CM11.1 was already very close to fully compliant.

CM11 overview: converted from padding/br layout to a standard `<ul>`; British spelling fixes ("organize"→"organise", "organized"→"organised").

CM11.1: collapsed doubled `<br><br>` to single `<br>` around three figures (no `float-none` added, per the updated guidance); tidied the placement of one Note: label so it reads as part of the Tags field bullet rather than as a floating sentence after the sublist.

Section 11 has no remaining open items.

## Section 12 (CM12, CM12.1)

Full mechanical style pass done across both files (one sub-tutorial). URL already confirmed, no changes needed. No blocking questions — CM12.1 was already very close to fully compliant.

CM12 overview: converted from padding/br layout to a standard `<ul>`; fixed an en dash (–) used as the description separator to the em dash (—) convention used elsewhere; lowercased the description's first letter to match every other overview entry.

CM12.1: collapsed one doubled `<br><br>` to single `<br>` around a figure. Everything else — field lists, Result:/Note: labels, breadcrumb bolding, Concepts prose — was already correct.

Section 12 has no remaining open items. This completes the full mechanical style pass through Section 12, the last section currently in the folder.

## CM5.2 and CM5.3: rebuilt on CM5.1's News/Events content

Following the CM5.1 redesign, Jeff asked to extend the same News/Events fixture (two categories, eight articles) into CM5.2 (Delete Articles) and CM5.3 (Archive Articles) rather than each tutorial having its own disconnected demo content.

**CM5.2:** The old Setup created a single throwaway "Troubadour" article, unrelated to any other tutorial. Replaced with a new "Retired Announcement" article (News category, Published) — a fresh throwaway article rather than reusing one of the 8 CM5.1 fixture articles, since delete is destructive and shouldn't consume content another tutorial depends on. Referenced by name throughout Moving to Trash / Find Trashed / Restore / Permanently Delete. Prerequisites now reference 5.1 Filter Articles instead of the generic "website with multiple articles" bullet. Removed all five figures (captured against the old article) — see screenshot recommendations below.

**CM5.3:** Previously had no Setup section at all. Archiving is non-destructive/reversible, so the archiving steps reference specific existing fixture articles by name instead of generic wording — "Draft Press Release" for edit-mode archiving, "Company Update" and "Local Meetup" for list-view (bulk) archiving. Prerequisites updated to match CM5.2. Removed all seven figures — see screenshot recommendations below. Note: these three fixture articles are left in Archived status at the end of the tutorial (matches original behaviour — the old version didn't restore state either).

**CM5.3 Concepts trim:** Jeff supplied replacement text to cut obscure/tangential content and sharpen the key points. Removed the standalone definitions of Articles, menu item, module, and Edit mode, plus "Archives are structured by year" and the cross-reference to 5.2's Trashed status. The four remaining paragraphs cover: what Archived does (hides without deleting; some menu items/modules can surface it on the frontend); that archived articles are filtered from the default backend list but findable via the Status filter; that archiving isn't the same as unpublishing, with Unpublished defined as the status that blocks public view; and the two ways to change an article's status (editor, or the Actions menu in the list).

**CM5.2 and CM5.3: real screenshots added.** Jeff shot and supplied all remaining images from a live site — 5 for CM5.2 (images/articles/325/) and 8 for CM5.3 (images/articles/326/), matching the recommendation lists above. Viewed each image before placing it; all matched the drafted step text with no wording corrections needed this time (unlike CM5.1's "Product Launch"/"Featured Articles" mismatches). One placement note: in CM5.2's "Moving the Article to Trash," the single Trash-selection screenshot content was split across two figures — trash_article.png (Actions dropdown open, about to click Trash) placed at the "Select Trash" step, and article_trashed_confirmation.png (confirmation banner, article gone from list) placed at the following "disappeared from list" step — since the one supplied image set covered both moments distinctly. CM5.1 and CM5.2 and CM5.3 all now have real screenshots throughout; no open items remain on any of the three except final review.

**CM5.3 revision (round 3, from live-site check):** In "Displaying Archived Articles via the Articles Module," corrected the actual field path — it's the <strong>Filtering Options</strong> tab (not <strong>Options</strong>), with an <strong>Archived Articles</strong> field set to <em>Only</em> (not a Status Filtering checklist as originally guessed). Removed the Menu Assignment step — it defaults to all pages, so setting it wasn't necessary. Renamed "Un-archive Articles" to "Republish Archived Articles" and replaced the one-line prose description with actual steps, mirroring CM5.1's Bulk Actions pattern: filter on Archived, tick the header checkbox to select all three, then Publish from the Actions dropdown.

**CM5.3 revision (round 2):** Jeff asked to drop "Archiving via a Menu Item" — it's just an alternate route to the same edit-mode form already demonstrated, so it added a screenshot and steps without teaching anything new. That also removed the only reason for the Setup section (the "Create a Menu Item" step existed solely to support that substep), so Setup is gone too — CM5.3 is back to having no Setup section, same as originally, but now the Steps reference fixture articles by name. Added a new "Archiving Multiple Articles from the Articles List" substep right after "Archiving an Article in Edit Mode," using the bulk-select-then-Actions-menu pattern (checking Company Update and Local Meetup, then Archive from Actions) — this folds in what used to be the separate "Archiving an Article from the Articles List" substep. "Displaying Archived Articles on Your Website" was split from a purely descriptive parent section with two prose-only h4 children into two full step-by-step h3 sections — "Displaying Archived Articles via a Menu" (create an Archived Articles menu item scoped to the News category, then view it on the frontend — deliberately excludes Local Meetup since it's in Events, demonstrating the category scoping) and "Displaying Archived Articles via the Articles Module" (create an Articles module with Status Filtering set to Archived only, then view it on the frontend). Both follow the established "tell the user exactly what to do" style rather than describing the feature in the abstract.

CM5.2's Concepts section is unchanged (general Joomla concepts, not tied to specific demo content). CM5.3's Concepts section was trimmed — see the Concepts trim note above.

### Screenshot recommendations — CM5.2 (images/articles/325/) — all placed with real images

1. After "Select Trash from the Actions options" (Moving the Article to Trash) — the Actions dropdown open with Trash highlighted, Retired Announcement selected.
2. After that same step's confirmation — the "article trashed" confirmation message.
3. After "Select Trashed from the Select Status list" (Find Trashed Articles) — the filtered list showing Retired Announcement as the only trashed article.
4. After "Click the Trashed symbol" (Restoring a Trashed Article) — the Trashed status icon in the list, before clicking.
5. After "Click the Delete button" (Permanently Delete an Article) — the warning/confirmation dialog before clicking Yes.

### Screenshot recommendations — CM5.3 (images/articles/326/), updated for round 3 — all placed with real images

1. After "Set the Status field to Archived" (Archiving an Article in Edit Mode) — the Status field set to Archived in Draft Press Release's edit form.
2. After "Select Archive from the Actions options" (Archiving Multiple Articles from the Articles List) — the Actions dropdown with Archive highlighted, Company Update and Local Meetup both checked/selected.
3. After "select Archived from the Select Status filter" (Finding Archived Articles) — the filtered list showing all three archived articles (Draft Press Release, Company Update, Local Meetup) with their archive icons.
4. After the menu-item creation steps (Displaying Archived Articles via a Menu) — the new-menu-item form showing Menu Item Type = Archived Articles and Select Category = News.
5. After "click the Archived News menu item" (same section) — the frontend page showing the two archived News articles.
6. After "Set the Archived Articles field to Only" (Displaying Archived Articles via the Articles Module) — the module's Filtering Options tab with Archived Articles set to Only.
7. After "View the site frontend" (same section) — the frontend sidebar showing the Archived Articles module with all three articles listed.
8. After "select Publish" (Republish Archived Articles) — the Actions dropdown with Publish highlighted, all three archived articles checked.

Open item: once Jeff supplies these images, place them with proper figure/figcaption markup (no `float-none`) and verify field names/values against the real screenshots, same as the CM5.1 verification pass (which caught "Product Launch" vs. "New Product Launch" and "Featured Articles" vs. "Featured").

## Section 2 (CM2.1–2.5): rebuilt on a shared Company/Team business fixture

Applying what we learned from the Section 5 redesign, Jeff asked for the same treatment on Section 2: unify the five sub-tutorials around content that's actually created once and reused/built upon, rather than each tutorial creating disconnected content (or, worse, silently reusing earlier content without crediting it, or reusing Joomla's built-in sample data instead of the tutorial's own).

**Problems found in the old versions:** 2.3 listed 2.1/2.2 as prerequisites but actually used Joomla's built-in sample "Joomla" category instead of anything created in those tutorials. 2.4 reused the *Mammals* category from 2.2 without listing it as a prerequisite. 2.5 introduced yet another disconnected one-off article instead of building on 2.1–2.3, and its category-shortcut half was purely hypothetical (pointed back at 2.2's steps rather than walking through it). 2.5 also had no Concepts section, unlike every other file in the section.

**First pass used a pet theme (Common Pets / Mammals / Dogs), superseded.** Jeff caught a real problem with it: assigning the *Common Pets* article to a *Mammals* category doesn't hold up, since "common pets" naturally includes non-mammals like fish — the fixture itself modeled a bad categorization choice. Redone with a business theme resembling Section 5's News/Events content, chosen specifically so nothing is a categorization stretch:

**New content matrix, built up tutorial by tutorial:**

- **2.1** creates the article *Company Overview* (an About-Us-style page — Article Text: "We are a company dedicated to providing quality products and services to our customers.") and the *About Us* Single Article menu item pointing to it. Kept the original "click Select, expand Articles, choose the type" long-form instruction for Menu Item Type here — it's the first time a reader encounters that popup, so it's spelled out in full. Every later tutorial that sets a Menu Item Type uses the terser `<em>Articles &gt; Type</em>` field-bullet shorthand instead, now that the mechanism has been taught once.
- **2.2** creates a *Company* category and now **two** sub-categories, *Team* and *Locations*, then assigns *Company Overview* (from 2.1) into *Company* — a natural fit, unlike the pet-theme version. **Revision:** the original draft left *Team* empty and didn't demonstrate any payoff from building the hierarchy, which Jeff flagged as a missed opportunity — creating structure with nothing to show for it. Fixed by adding a second sub-category (*Locations*) and a new "Add Articles to the Sub-categories" substep that creates one article for each (*Meet the Team* in Team, *Our Locations* in Locations), plus a closing paragraph explaining that we've now built a small real structure and pointing ahead to 2.3, where menu items will put it to work on the frontend. This gives the tutorial more to actually do, reinforces why the hierarchy matters, and motivates continuing to the next tutorial for the payoff.
- **2.3** replaces the Joomla-sample-data approach with a new Setup section, "Add More Articles to Company," which adds *Our Mission* and *Our History* (both Category: Company) so the category has three real, thematically consistent articles — About/Mission/History is a natural trio for a company section. The two menu items are named *Company Articles Blog* and *Company Articles List*, both pointed at *Company*. Concepts now calls out that *Company Overview* is reachable two ways after this tutorial — directly via 2.1's *About Us* link, and as part of the *Company* category listing — a small bonus teaching point that fell out of the redesign. **Revision:** since 2.2 now builds *Team* and *Locations* sub-categories with an article each, "Create a Category Blog Layout" adds two steps exploring that payoff live on the frontend — the blog page also shows links to both subcategories; step 6 clicks into *Team* to see *Meet the Team*, and step 7 uses the breadcrumb to return to *Company Articles Blog* before clicking into *Locations* to see *Our Locations*. This is the frontend payoff 2.2's closing paragraph pointed ahead to. "Create a Category List Layout" gets a lighter touch on the same point — Jeff didn't want a full step-by-step exploration repeated here, so its final step just notes that the list layout also shows the two subcategories and invites the reader to explore them if they like, rather than walking through it again.
- **2.4** no longer invents a "Marsupials"-style new article — it features *Company Overview* itself (already in *Company* since 2.2), reusing existing content rather than piling on more. Prerequisites now correctly credit 2.1 and 2.2. Renamed the second substep to "Feature the Company Overview Article" to match. **Revision:** dropped the Filter Options step — Jeff felt it wasn't essential here and filtering gets proper coverage in 5.1 Filter Articles (added as a Concepts cross-reference instead of a walked-through step). Added a step after viewing the site noting that the Featured column shows a gold star for Company Overview back in the article list, then a new substep, "Feature a Second Article from the List," which features *Meet the Team* (the Team sub-category article from 2.2) by clicking its Featured-column star directly — demonstrating the list-icon toggle as an alternative to editing the article, and reinforcing that featuring works the same for sub-category articles as it does for the parent category. Ends with a second site view showing both featured articles together.
- **2.5** makes both shortcut variants concrete instead of one being hypothetical: the article half creates a new *Careers* article via Save to Menu (a plausible new page, distinct from the Company-category trio); the category half actually creates a new *Services* category via *Save to Menu as List*, walking through the real steps end-to-end, with *Save to Menu as Blog* explained as the same process via the alternate dropdown option (to avoid creating a redundant second category just to demonstrate an identical mechanism). Added a Concepts section, which this file was previously missing.

**Style unification applied throughout:** "Click on the New button" → "Click New" (and similar "click on X" → "click X" trims) to match the CM10/CM5 precedent; "In the left side menu of the administrator homepage" / "In the left side menu" → "In the Administrator Menu" for consistency with the standardized term used everywhere else; menu item type fields written as terse `<em>Articles &gt; Type</em>` bullets after the mechanism is taught once in 2.1. All old figures removed pending new screenshots (see recommendations below).

**Image folder numbers confirmed via the Tutorial URL Reference spreadsheet**, which Jeff has now filled in with each article's Joomla ID in column I (images are organized by that ID, same convention as Section 5's 324/325/326): CM2.1 → 282, CM2.2 → 289, CM2.3 → 292, CM2.4 → 309, CM2.5 → 290. These match what the old CM2.2–2.5 files already used, confirming the pattern; 2.1's 282 is newly identified since that file had no screenshots before.

### Screenshot recommendations — CM2.1 (images/articles/282/, no prior screenshots)

1. After the new-article step — the filled-in new-article form (Title: Company Overview, Article Text visible).
2. After the new-menu-item step — the filled-in new-menu-item form showing the Single Article type popup and Company Overview selected.
3. After the final step — the frontend About Us page showing the published article.

### Screenshot recommendations — CM2.2 (images/articles/289/)

1. After "Click Save & Close" for Company — the new-category form filled in with Title: Company.
2. After the Locations sub-category step — the new-category form filled in with Title: Locations, Parent: Company (also shows the Team sub-category form pattern, one step earlier).
3. After "Set the Category field to Company" — the Company Overview edit form with Category set to Company.
4. After the Add Articles to the Sub-categories substep — the categories list showing Company with Team and Locations nested under it, each with an article count of 1.

### Screenshot recommendations — CM2.3 (images/articles/292/)

1. (Optional) After the Setup section — the Articles list filtered/sorted to show all three Company articles.
2. After the Category Blog menu item is configured — the filled-in menu item form (Title: Company Articles Blog, Type: Category Blog, Category: Company).
3. After "view a blog layout" — the frontend Company Articles Blog page showing all three articles, with the Team and Locations subcategory links visible.
4. After "Click the Team subcategory link" — the frontend Team subcategory page showing the Meet the Team article.
5. After "click the Locations subcategory link" — the frontend Locations subcategory page showing the Our Locations article (also a good spot to catch the breadcrumb, e.g. Home / Company Articles Blog / Locations, in the same shot).
6. After the Category List menu item is configured — the filled-in menu item form (Title: Company Articles List, Type: Category List, Category: Company).
7. After "view a list layout" — the frontend Company Articles List page showing all three articles and the two subcategory links (no separate subcategory-exploration shots needed here, unlike the Blog layout — the step just mentions they're there).

Open items to verify against the real screenshots: whether the menu item field is actually labeled "Choose a Category" or just "Category" (carried over from the original file without a screenshot to confirm); and whether the subcategory links on the blog page, and the breadcrumb label, read exactly as described (e.g. confirm "Company Articles Blog" is what actually shows in the breadcrumb, not the category name).

### Screenshot recommendations — CM2.4 (images/articles/309/)

1. In "The Home Menu is a Featured Articles Menu Item" — the menu items list showing Home's type as Featured Articles.
2. After "Set the Featured field to Yes" — the Company Overview edit form with Featured set to Yes.
3. After "View the site" (first one) — the homepage showing Company Overview as a featured article.
4. After "Return to the backend article list" — the article list with the gold star visible in the Featured column next to Company Overview (ideally with a not-yet-featured article's hollow/outline star also visible for contrast).
5. After "click the icon next to Meet the Team" — the article list right after the click, showing the icon now gold for Meet the Team.
6. After the second "View the site" — the homepage showing both Company Overview and Meet the Team as featured articles.

### Screenshot recommendations — CM2.5 (images/articles/290/)

1. After "select Save to Menu" (Save an Article to a Menu) — the Save & Close dropdown open with Save to Menu highlighted.
2. After the prefilled-fields step — the prefilled Single Article menu item form for Careers, required fields visible.
3. After "select Save to Menu as List" (Save a Category to a Menu) — the Save & Close dropdown open on the Services category form, with Save to Menu as List highlighted.
4. After the prefilled-fields step — the prefilled Category List menu item form for Services.

Open item: once Jeff shoots and supplies these images (folder numbers now confirmed above), place the figures and verify field names/values against the real screenshots (same verification pass as every prior section) — including the "Choose a Category" vs. "Category" label question flagged under CM2.3.

## Section 2: all real screenshots placed and verified

Jeff shot and supplied all remaining images across the section — 3 for CM2.1, 4 for CM2.2, 7 for CM2.3, 6 for CM2.4, 4 for CM2.5 (24 total). Viewed every image before placing it, same verification pass as every prior section. Findings:

- **"Choose a Category" confirmed correct** — visible verbatim in the CM2.3 menu item screenshots, resolving the open item flagged earlier.
- **CM2.3 breadcrumb confirmed** — the Team/Locations subcategory pages really do show "Company Articles Blog" as a clickable breadcrumb link back to the parent category page, exactly as drafted.
- **CM2.4 revised, per Jeff's note on the screenshot:** the menu items list already shows "Articles » Featured Articles" beneath the Home title without opening the item — step 3 of "The Home Menu is a Featured Articles Menu Item" reworded from "Observe that..." to "Look at the Home row... the list already shows..." to reflect that this is visible at a glance. Also added the "Article featured." confirmation message to the result of the list-icon-click step, since the screenshot showed it.
- **CM2.5 revised, per Jeff's notes on the screenshots:** added <strong>Category: Company</strong> to the Careers article's field list in "Save an Article to a Menu" — Jeff's screenshot showed it assigned to Company, and leaving it out of the tutorial text would have made the screenshot and text disagree. Also changed "Select Article: the link to the article" to the literal value "Careers", and "Menu: the default menu, most likely Main Menu" to the literal "Main Menu" — both confirmed by the real screenshot instead of hedged/generic language.
- **Minor artifact, not corrected:** the CM2.1 new-menu-item screenshot shows "Household Pets" in the Ordering dropdown on the right — a leftover from Jeff's earlier pet-themed test site build, before the re-theme to the Company/Team content. Doesn't affect anything the tutorial text claims (we don't reference menu ordering), so no text change was needed, but flagging it in case Jeff wants to clean up that test site's leftover menu item.

All five Section 2 files are now complete with real, verified screenshots — no open items remain.

## Section 3 (CM3.1–3.5): one running article, replacing five disconnected demos

Jeff asked for the same "business content" theme used in Sections 2 and 5, applied to Section 3 (the WYSIWYG editor tutorials) — plus a much deeper rebuild of CM3.3 (Lists) specifically.

**The problem:** none of the five sub-tutorials kept what they created. CM3.1 ended with Cancel (discarding the practice article). CM3.2 explicitly said "Close the article without saving." CM3.3's list demo article's fate was never specified. CM3.4 never closed its demo article cleanly. CM3.5 explicitly created a demo article "for demonstration purposes, and then delete[d] the article." Nothing persisted, and nothing tied the five tutorials together.

**The fix:** a single article, <em>Our Services</em> (a generic professional-services company), created in 3.1 and reopened and extended in each subsequent tutorial, finishing as a complete, real piece of content by the end of 3.5. Approved by Jeff before implementing, including the article topic, the three service-line names, and the 3.4 hyperlink target.

- **3.1 (Bold, Italic & More):** Keeps the "try every toolbar button" exploration (bold/italic/underline/strikethrough) on throwaway practice text, then writes the article's real opening paragraph with bold on the value-prop phrase and italic on a supporting phrase. Ends with Save &amp; Close instead of Cancel. Concepts gained a note that underline is conventionally reserved for links, so using it elsewhere for emphasis risks confusing readers.
- **3.2 (Headings):** Replaced the generic "Transportation / Aircraft / Watercraft" example with the real outline: H2 <em>Consulting</em>, <em>Implementation</em>, and <em>Support</em>, each with a short paragraph; <em>Consulting</em> and <em>Implementation</em> each get an H3 sub-heading (<em>What's Included</em> and <em>Getting Started</em>) left empty for 3.3 to fill in. The H1/H2/H3/H4-depth demonstration is preserved as a throwaway aside (create a practice H4, then delete it) so the real article doesn't gain a heading level it doesn't need.
- **3.3 (Lists):** Full rebuild — see below.
- **3.4 (Links):** Adds one real hyperlink instead of a disconnected demo article: a sentence appended to the end of the <em>Support</em> paragraph ("This site itself is proudly built on Joomla...") with <em>Joomla</em> linked to https://www.joomla.org. Concepts ties this back to the existing WebAIM link-text citation — linking a meaningful word instead of "click here."
- **3.5 (Tables):** Adds a final H2, <em>Plans &amp; Pricing</em>, and a 4×4 Basic/Standard/Premium comparison table (consulting hours, implementation support, response time), using the existing table-formatting steps (borders, header row, cell padding) unchanged. The intro no longer says the demo article gets deleted afterward — this is the capstone step, and the closing line cross-references 2.1 Article &amp; Menu Item for anyone who wants to actually publish the finished article.

Also standardized mechanical style across all five files while rewriting them, consistent with prior sections: "Click on the New button" → "Click New" and similar trims, "In the left side menu..." → "In the Administrator Menu" (3.4 and 3.5 both had the old phrasing). 3.4/3.5's Prerequisites also dropped the "Administrator access to a Joomla site (version 5 or above)" boilerplate bullet to match the simpler Prerequisites style used in 3.1–3.3.

**All old figures removed** across all five files — they showed either the wrong content entirely (headings screenshots showed Transportation/Aircraft, not Consulting/Implementation) or, per Jeff's specific complaint about CM3.3, were "extremely small and not the style of other tutorials" (icon-only crops as small as 99×48 and 134×63, versus the full-editor-context screenshots like 1770×1356 used in 3.4/3.5 previously). New screenshots needed throughout — recommendations below, sized and framed like the rest of the project's screenshots (full editor/browser context, not cropped icons).

### CM3.3 (Lists) — the six techniques

Jeff asked for six specific things to be demonstrated, replacing the old structure where "Unordered List" and "Ordered List" were two nearly identical sections (build via paragraphs, select, click icon) with the second just noting "works the same for ordered." The new version distributes all six across the two real lists instead of repeating everything twice:

1. Building a list from separate typed paragraphs, then selecting and converting (the original method, kept) — used for <em>What's Included</em> (Roadmapping / Technology audit / Vendor selection support).
2. Building a list by typing directly into it (click the list icon on an empty line, then type with Return between items) — used for <em>Getting Started</em>.
3. Pressing Return twice to exit a list back into a normal paragraph — demonstrated at the end of typing <em>Getting Started</em>.
4. Highlighting a list and clicking the opposite type's icon to switch it — demonstrated on <em>Getting Started</em> (bullets, then back to numbers, ending in the correct state since these are sequential steps).
5. Tab / Increase Indent to create sub-items — demonstrated by breaking <em>Environment setup</em> into two nested sub-items.
6. Unordered sub-items nested inside an ordered list — the same two sub-items get converted to bullets while the parent stays numbered, explicitly called out as the exact pattern this whole documentation project uses (numbered steps, bulleted details).

Concepts closes with the semantic-markup point Jeff wanted: ordered vs. unordered communicates sequence-matters vs. sequence-doesn't, screen readers announce list type and item count, and this documentation's own numbered-steps-with-bulleted-details convention is a real-world example of nesting the two types together. The alternate-numbering-style aside (letters, roman numerals via the dropdown arrow) was kept as a brief closing note rather than a full walkthrough, since it wasn't one of the six requested items.

### Screenshot recommendations — CM3.1 (images/articles/293/)

1. After trying Bold/Italic/Underline/Strikethrough on practice text — the editor showing practice text in all four formats, with the popup toolbar visible.
2. After the normal paste — the pasted example text showing it kept its bold/italic formatting.
3. With Paste as text toggled on — the toolbar showing the icon highlighted (similar to the screenshot Jeff already supplied for this note).
4. After writing the real intro paragraph — the editor showing the finished paragraph with bold and italic phrases visible.

### Screenshot recommendations — CM3.2 (images/articles/294/)

1. After creating the Consulting H2 via the formatting dropdown — dropdown open, Headings > Heading 2 visible.
2. After creating the What's Included H3 via the popup menu — popup showing H2/H3 icons over the highlighted text.
3. After all three H2 sections and two H3 sub-headings are in place — full outline visible in the editor.
4. After clicking Toggle Editor — the HTML source showing the heading tags.

### Screenshot recommendations — CM3.3 (images/articles/285/)

1. After typing the three What's Included items as separate paragraphs.
2. After converting them to a bulleted list.
3. After typing the Getting Started list directly (items typed, numbered).
4. After pressing Return twice — cursor now in a normal paragraph below the finished list.
5. After switching Getting Started to bullets, then back to numbers (one or two shots, showing the toolbar icons).
6. After adding and indenting the two Environment setup sub-items, before converting them to bullets.
7. After converting the sub-items to bullets — the final nested ordered/unordered list.

Please shoot these at full editor width/context, not cropped to just the icon or list — that's the specific complaint about the old versions.

### Screenshot recommendations — CM3.4 (images/articles/296/)

1. The Insert/Edit link form with the URL and Text to display (Joomla) filled in.
2. The Support paragraph showing the saved Joomla hyperlink in the text.
3. The right-click context menu (Link / Remove Link / Open Link) over the Joomla link.

### Screenshot recommendations — CM3.5 (images/articles/297/)

1. The table size-picker grid.
2. The filled-in, unformatted table in Preview (no borders).
3. The Cell Properties > Advanced border settings (1px, Solid).
4. The header row formatting (Cell Type = Header Cell, Horizontal align = Center).
5. The final formatted table in Preview — borders, header row, padding all applied.

Open item: once Jeff shoots and supplies these images, place them and verify field names/values against the real screenshots, same as every prior section.

**CM3.1 revision:** Jeff pointed out steps 4/5 never explained that the TinyMCE toolbar starts collapsed to a single row and needs the ellipsis (⋯) icon clicked to reveal the second row of tools (headings, lists, links, tables, etc.) — a real gap, since 3.4 and 3.5 both already say "expand the toolbar by clicking the ellipsis" as if it's already been taught. Added a step for this in 3.1 (first exposure gets the full explanation, matching the pattern used elsewhere in this project — e.g. Menu Item Type in 2.1), with a note that later tutorials will refer back to this step rather than re-explaining it. 3.4/3.5's existing terse phrasing didn't need to change, since it now correctly assumes the reader has done 3.1 first.

**CM3.1 revision 2:** Jeff's screenshot of the popup toolbar showed more than the three icons the text claimed (bold, italic, underline) — it also had H2/H3 heading shortcuts, a link icon, and a blockquote icon. Reworded to "bold, italic, underline, and a few other commonly-used tools" rather than listing an exact icon set that could vary by version/configuration.

**CM3.1 revision 3:** Jeff asked to add a demonstration of the <strong>Paste as text</strong> tool (a clipboard-with-"T" icon in the expanded toolbar) in place of the old plain "delete the practice text" step. New flow: copy a short bold/italic example phrase given right in the tutorial text, paste it normally (formatting carries over — not always wanted, e.g. pasting from Word or a web page), delete/undo it, toggle Paste as text on, paste the same text again (this time plain, no formatting), toggle it back off, then delete everything before moving on to writing the real opening paragraph (which still gets its formatting applied manually via highlight-and-click, unchanged). Added a matching Concepts paragraph on why Paste as text matters, and folded a mention of it into the intro paragraph. This also gave the toolbar-expansion step from the prior revision an early payoff, since Paste as text lives in the second row.

**CM3.1 revision 4:** Jeff refined the paste demo further — removed the "delete or undo" step that used to sit between the two pastes, and had the second (Paste as text) paste land directly below the first instead of replacing it. Both pastes are now visible on screen at once, stacked, so the formatted-vs-plain difference is obvious without needing to remember what the first one looked like. The final "type the real paragraph" step was also reworded to "Type (or copy and paste as text) the following," inviting the reader to reuse the technique they just learned on the real content, not just the throwaway example.

**CM3.1 revision 5:** Removed the closing Concepts line, "There are a number of very powerful features that are explored in other tutorials." — a vague, generic statement that didn't emphasize or expand on anything actually covered in this tutorial. Concepts now ends on the Paste as text paragraph, which is substantive.

**CM3.1: real screenshots placed.** Jeff supplied all four (images/articles/293/formatting_practice.png, paste_with_formatting.png, paste_without_formatting.png, article_introduction.png). Viewed each before placing. One genuine finding, not an error: the normal-paste screenshot shows the example text landing as a numbered list item, not a plain line — because Jeff copied it straight from this tutorial page, where the example sits inside a numbered step. Rather than treat this as a mismatch to fix, added a Note explaining it: paste carries over more than character formatting, it can carry over structure too (like list numbering), which is actually a stronger demonstration of the point than a plain-text example would have been. The Paste as text screenshot confirms the second paste has no numbering at all, reinforcing the same point. CM3.1 is now complete with real, verified screenshots.

**CM3.2 revision:** Jeff's detailed feedback, all applied:
- Steps 11 and 14 ("Press Return, set the format to Paragraph, and type...") no longer instruct setting the format manually — Return already reverts to Paragraph after a heading, as already noted at step 7. Step 11 now carries a bullet noting this explicitly ("As in step 7, the format automatically returns to Paragraph..."); step 14 doesn't repeat the note since it's now established.
- Removed the closing "Clearly we can simply keep going here..." paragraph (including its H4-depth practice demonstration) entirely — Jeff felt it wasn't needed and asked to fold the underlying point into Concepts instead. Added to Concepts: you can nest as many heading levels as an outline needs, and that the popup toolbar only offers H2/H3, so H4 and deeper require the formatting dropdown.
- Moved "Note the visual differences between the headings..." from a trailing paragraph into Concepts, merged into the existing "headings are specific typographical elements" paragraph.
- "Click the blue Toggle Editor..." is now a real numbered step (step 17 in the final count) instead of trailing prose, with a new step 18 for toggling back. Added a mention that the editing toolbar disappears in this view. Researched the proper name via web search: Joomla's Toggle Editor button switches between TinyMCE and <em>No Editor</em> mode (a plain textarea showing raw HTML) — used "No Editor" as the name, with a new Concepts paragraph explaining what it's for.
- New content added as steps 15–16 (kept dense/combined, matching this tutorial's existing step style, so Toggle Editor lands on step 17 as Jeff expected): step 15 covers the toolbar preview icon (rough, unstyled, reflects unsaved editor content); step 16 covers the top-of-page Preview button (styled, reflects last-saved version only) — click it now to see just the 3.1 paragraph, close it, Save (not Save & Close), Preview again to see the full outline. Added matching Concepts paragraph distinguishing the two preview mechanisms. Chose not to break this into its own h3 subsection — doing so would restart the step numbering per this project's established h3-per-tutorial convention, which would prevent Toggle Editor from landing on step 17; used a bolded lead-in ("Preview your progress.") inside step 15 instead, matching the sub-grouping style already used in CM3.5.
- Combined "Always use heading elements..." and "Never use heading elements to simply emphasise text." into a single Concepts paragraph, per Jeff's suggestion.
- "Save & Close" also pulled into the ol as step 19 (previously trailing prose), for consistency with CM3.1's ending pattern.

**CM3.3: real screenshots placed.** Jeff supplied all eight (images/articles/285/selecting_list_item_paragraphs.png, clicking_bullet_list_icon.png, typing_numbered_list.png, numbered_list_finished.png, converting_to_unordered_list.png, converting_to_ordered_list.png, indenting_sub_items.png, sub_items_to_bullets.png — the file on disk for the fifth recommendation item is named converting_to_unordered_list.png, not converting_to_numbered_list.png as typed in Jeff's message; used the real filename). Viewed each before placing. One genuine finding: the toolbar icon tooltips read <strong>Bullet list</strong> and <strong>Numbered list</strong>, not "Unordered list" and "Ordered list" as drafted — corrected throughout the Steps and Concepts sections (the surrounding prose describing list *types* as "ordered"/"unordered" was left as-is, only the icon names changed). Also confirmed the sub-item indent behavior exactly as drafted: indenting nests Provision hosting/Configure DNS as their own numbered sub-list, and the parent list renumbers so First milestone review becomes item 3 again. CM3.3 is now complete with real, verified screenshots — no open items remain.

**Heading semantics verified.** Jeff asked to double-check CM3.2's "only one H1, work with H2 and below" claim against the actual rendered page source for 3.3 Lists. Confirmed: within the article body, the heading hierarchy is correct (single H1 from the article title, H2 siblings for Prerequisites/Steps/Concepts, H3 children under Steps only, no skipped levels). Flagged one nuance — the site template itself adds a second H1 outside the article body (the header's logo/site-name link) — but agreed with Jeff this is too much detail for a tutorial and isn't being added to CM3.2. No file changes from this check.

**CM3.4 revisions:**
- Step 4: removed "itself" from "This site itself is proudly built on Joomla..." — reads more naturally as "This site is proudly built on Joomla...".
- Steps 5–6: Jeff's screenshot showed that highlighting the word <em>Joomla</em> pops up the same popup toolbar taught in 3.1/3.2 (B/I/U/H2/H3/link/quote icons), and it includes a link icon directly — no need to expand the main toolbar via the ellipsis first. Reworded from "Expand the toolbar by clicking the ellipsis points, then click the Insert/Edit link icon" to two steps: selecting the word (now notes the popup toolbar appears), then clicking the link icon in that popup toolbar. Matches the icon-naming caution from CM3.1/3.3 — didn't invent a tooltip name for it, just called it "the link icon."

**CM3.4: real-world Preview/framing issue found and fixed.** Jeff tried the tutorial's own link on the live site and hit Firefox's "Can't Open This Page" error when clicking the Joomla link from inside Preview — joomla.org refuses to display itself inside a frame, and Joomla's Preview button renders the article inside one. Setting the link's Target to open in a new window fixed it for Jeff. Applied that as a step: added a Target sub-bullet under the URL-entry step (with a Note explaining why), updated the Preview-testing step's Result to reflect the link now opening in a new tab, and extended the Concepts paragraph on new-tab links to cover this as a second reason (alongside the existing "supplemental content" one) — external links are safer opened in a new tab specifically because some sites block framing. Open item: the field name "Target" and value "Open in new window" are a standard-TinyMCE guess, not yet confirmed against this site's actual Insert/Edit Link form — worth checking against the CM3.4 screenshot recommendation #1 (the link form) once Jeff shoots it.

**CM3.4 revision:** Jeff confirmed "click just to the right of the Joomla link, then right-click" was unnecessary — right-clicking the word itself opens the link options regardless of exact cursor placement first. Simplified to "right-click the Joomla link."

**New pattern: incidental UI familiarity steps.** Jeff added a step after "Click Our Services to reopen it for editing" instructing the reader to drag the editor's Resize handle (bottom-right corner of the text area) to see more of the article while working — a genuinely useful habit, not strictly necessary for this tutorial's actual task. Jeff's rationale: on a short tutorial like this one, folding in a small, real, useful UI action (without calling explicit attention to it as its own concept) is a good way to build reader familiarity with the editor over time. He said he'll be watching for more opportunities like this across the remaining tutorials — worth keeping in mind for future edits/reviews, not just applying once here.

**CM3.4 addition:** second incidental-familiarity step added right after the Resize step — toggle the <strong>Fullscreen</strong> icon in the toolbar to expand the editor to fill the browser window, then toggle it back off before continuing. Same rationale as the Resize step: real, useful, not central to this tutorial's actual task (adding a link), folded in without a separate Concepts callout. Jeff confirmed via screenshot: tooltip reads "Fullscreen (⌘⇧F)" — icon description and keyboard shortcut both updated to match exactly.

**CM3.4: real screenshots placed, field-name corrections.** Jeff supplied all three (images/articles/296/insert_edit_link_form.png, joomla_link.png, right_click_link.png). Viewed each before placing — several drafted guesses turned out wrong:
- The field I'd called <strong>Target</strong> is actually labeled <strong>Open link in...</strong>, and its value is <em>New window</em>, not "Open in new window." Fixed everywhere it's referenced (the URL step, the Preview-testing step's Result).
- The right-click menu's three options are <strong>Link...</strong> (with a "⌘K" shortcut shown, reopens the Insert/Edit Link form — not a separate "link editing menu"), <strong>Remove link</strong>, and <strong>Open link</strong> — different capitalization than drafted ("Link"/"Remove Link"/"Open Link").
- The screenshot happened to show the <strong>Title</strong> field filled in (<em>The Joomla Website</em>), which the Concepts section already discusses conceptually but no step had ever demonstrated — added it as a real field-bullet in the URL step so the concept has a matching action, consistent with how CM3.3 gives its "alternate numbering styles" aside a brief hands-on mention too.

CM3.4 is now complete with real, verified screenshots — no open items remain.

**CM3.2: real screenshots placed.** Jeff supplied all four (images/articles/294/applying_h2.png, applying_h3.png, article_in_editor.png, article_html.png). Viewed each before placing. All matched the drafted text with no corrections needed this time: applying_h2.png confirms the formatting dropdown flow (Headings submenu, Heading 2 checked, Consulting typed below); applying_h3.png confirms the popup toolbar's exact icon set — bold, italic, underline, H2, H3, link, quote — matching the "a few other commonly-used tools" wording already used in CM3.1; article_in_editor.png shows the full outline with both sub-headings still empty, placed after step 14 (before the new Preview steps); article_html.png confirms "No Editor" mode shows raw HTML directly in a plain textarea, with the Toggle Editor button still visible/labeled below it — validates the "No Editor" terminology used in the text and Concepts. CM3.2 is now complete with real, verified screenshots — no open items remain, aside from Jeff's live-site confirmation of the preview-icon behavior described in steps 15–16 (not yet visually confirmed by a screenshot).

**CM3.5: real screenshots placed, several corrections.** Jeff supplied all six (images/articles/297/inserting_4_by_4_table.png, unformatted_table.png, right_click_cell_cell_properties.png, adding_borders.png, header_cell_properties.png, preview_table.png — recommendation #3 mapped to two files, matching the earlier CM3.4/CM3.5 pattern of one recommendation covering more than one shot). Viewed each before placing. Several real findings:
- The heading Jeff actually typed on the live site is <strong>Plans and Pricing</strong>, not "Plans &amp; Pricing" as drafted — changed throughout (this was the one literal value in the file using an ampersand, so a simple find-and-replace was safe).
- The contextual table toolbar (add/delete row/column icons) appears <em>above</em> the table when the cursor is in a cell, not below as drafted — fixed.
- Reaching cell formatting is a three-step menu path, not a direct one: right-click → hover <strong>Cell</strong> → click <strong>Cell properties</strong> (lowercase "properties," matching the real menu item; the resulting window's own title is "Cell Properties," title case, which is what's referenced once it's open) — fixed in both the border step and the header-row step, which had already gotten the mechanism half-right.
- Real field/value casing from the Cell Properties screenshots: <strong>Cell type</strong> (not "Cell Type"), value <em>Header cell</em> (not "Header Cell"); <strong>Border width</strong>/<em>1px</em> and <strong>Border style</strong>/<em>Solid</em> confirmed exactly as drafted. Also fixed "Table Properties" → "Table properties" in the cell-padding step for the same menu-casing reason.
- Not corrected, just noted: the live test data shows a typo, "Cmail + calls" instead of "Email + calls," visible in three of the six screenshots (Jeff's own data-entry slip while testing, not a tutorial-text error — the instructed value is already correct). Not worth a reshoot on its own; flagged in case Jeff wants to fix it next time he's on the live site.

CM3.5 is now complete with real, verified screenshots. This completes Section 3 (CM3.1–3.5) end to end — no open items remain across the whole section.

## Section 4 (CM4, CM4.1–4.3): astronomy theme, real category, CM4.3 full redesign

Jeff asked for the same treatment as Sections 2/3/5: build real, connected content instead of disconnected demos. He assessed CM4.1 and CM4.2 as "reasonably fit" himself and asked me to confirm; CM4.3 he flagged as needing a full rebuild. Also asked for a category to be introduced (subtly, by example, not with a big explanation) and reused across the section, and for me to source suitable images from Wikimedia Commons once the theme was settled. He liked the astronomy theme already present in the old CM4.1/4.2 drafts, so kept it.

**Important discovery before writing anything:** none of the three files' referenced screenshots actually exist — `images/articles/303/`, `304/`, and `287/` (CM4.1/4.2/4.3's folders) are all absent from the Tutorials image folder entirely. These were leftover fabricated/placeholder paths from before this project's real-screenshot workflow existed (Section 4 was flagged much earlier as "draft files, untouched" when the URL reference spreadsheet was built). Stripped every `<figure>` in all three files rather than leave dead references, matching this project's standing rule of never leaving fabricated image paths in place. Screenshot recommendation lists for all three are below, same as every other section's first pass.

**My analysis of CM4.1 and CM4.2, confirmed with Jeff before implementing:**
- CM4.1: good foundation (real Wikimedia sourcing, clean upload/insert/caption flow) but had no category, and only ever showed one image, captioned and centered. Needed to add: a category, a second image demonstrating no caption + float + border.
- CM4.2: agreed no article is needed — it's genuinely just about the Media component, and its telescope theme already fits under the astronomy umbrella (telescopes are the instruments). Only needed mechanical fixes.

**CM4.1 (Images in Articles):** Renamed the article from generic "Astronomy" to <em>Crab Nebula</em> (matching what it's actually about) and added a Category field, creating a new <em>Astronomy</em> category via Content &gt; Categories &gt; New first — matching the exact mechanism already established in CM2.2, not an invented inline-from-article-form shortcut. Added a Note that the <em>Astronomy</em> media folder and the <em>Astronomy</em> content category are two different systems that happen to share a name here, since the coincidence could otherwise read as a mistake. Added a second h3 substep, "Add a Second Image, Floated with a Border" — types a supporting sentence, embeds an Orion Nebula image without checking Show caption (contrast with the first image), then floats it with a border. The exact mechanism for float/border is flagged as unverified in the tutorial text itself (a Note pointing at "an Advanced tab, a Class or Style option, or alignment icons," since I don't yet know which one this Joomla version/config actually uses) — this needs a real screenshot to pin down precisely, more so than most guesses in this project since it's genuinely new territory (first time this project has touched the Insert/Edit Image dialog's alignment/border controls). Concepts gained two new paragraphs: caption guidance (use when it adds context, skip when self-explanatory) and float/border as visual choices. Attribution trimmed to just the two images actually used here (Crab Nebula, Orion Nebula) — moved Jupiter and Andromeda Galaxy's attribution to 4.3, where they're actually used now (they'd been sitting unused in 4.1's Attribution list since some earlier draft).

Also fixed: the Prerequisites' "download this image" links pointed at the same non-existent `images/articles/303/` folder — switched to direct links to each image's Wikimedia Commons page instead of assuming Jeff has self-hosted copies at a path that doesn't exist.

**CM4.2 (Managing Media):** Only mechanical fixes, structure/content otherwise untouched per Jeff's own assessment. Removed a stray `<span style="text-decoration: underline;">` around "immediate and irreversible" — violated this project's own house style (CM3.1's Concepts section explicitly argues against using underline for anything but links). Same Prerequisites fix as 4.1: the three telescope images and the PDF now link directly to their real Wikimedia Commons pages / the actual NASA-hosted PDF URL (already used in this file's own Attribution section) instead of a non-existent local path. Left the unused "Radio Telescopes" sub-folder as-is — flagged as optional/minor, not worth the scope creep on a file Jeff already signed off on.

**CM4.3 (Intro and Full Article Images): full redesign.** Reuses the <em>Astronomy</em> category and <em>Crab Nebula</em> article from 4.1 rather than the old "Demo article images" / "Demo Stuff" placeholder content. Adds two more articles, <em>Jupiter</em> and <em>Andromeda Galaxy</em>, giving the category exactly three articles — matching what the old draft claimed ("this category has three articles") but never actually built. Dropped the old two-column/leading-article-plus-four-intro-articles menu item configuration entirely; the Category Blog menu item now uses defaults, per Jeff's own instinct that the layout customization wasn't earning its keep anywhere later in the tutorial.

Demonstrates the intro-image/full-article-image independence Jeff asked for by treating <em>Crab Nebula</em> as the deliberate contrast case: its Full Article Image is the same close-up already embedded in its body text from 4.1, but its Intro Image is a different photo entirely (a multi-telescope composite) — so the reader sees one image on the category blog listing and a different one after clicking in. <em>Jupiter</em> and <em>Andromeda Galaxy</em> then demonstrate the more common pattern — same image reused for both Intro and Full Article Image — including a step showing how to select an already-uploaded image a second time rather than uploading it twice. Also added a Float step on Jupiter's intro image (mirroring the float concept from 4.1, now applied to a category-blog image instead of an in-body one) and a brief Note on the <strong>No description</strong> checkbox for decorative images. Both of these, like CM4.1's float/border step, are flagged as needing live confirmation — I know "No description" is real Joomla terminology (it survived from the original draft and matches what I know of core Joomla), but "Float" as a literal field name/location for Intro/Full Article Image is a plausible-but-unconfirmed guess.

**Image sourcing.** Crab Nebula's original close-up image (NASA, already cited) stays as the Full Article Image. New Wikimedia Commons image sourced for the Intro Image contrast: <a href="https://commons.wikimedia.org/wiki/File:Crab_Nebula_NGC_1952_(composite_from_Chandra,_Hubble_and_Spitzer).jpg">Crab Nebula NGC 1952 (composite from Chandra, Hubble and Spitzer)</a>, public domain, NASA/ESA/CXC/JPL-Caltech — a genuinely different-looking (multi-wavelength, different color palette) photo of the same object, which is more honest than using an unrelated image just to prove the point. Jupiter and Andromeda Galaxy reuse the two images already cited (but previously unused) in 4.1's old Attribution list — Jupiter rendered with Blender (Wikideas1) and the Luc Viatour Andromeda Galaxy photo.

**Open items, all needing live-site/screenshot confirmation (none blocking, but flagged prominently since this is new UI territory for the project):**
1. CM4.1's float/border mechanism for embedded images — exact dialog, tab, and field names unconfirmed.
2. CM4.3's Float option location/name for the Intro Image — unconfirmed.
3. All screenshot recommendations below are unfulfilled — none of Section 4's real screenshots exist yet.

**Correction: prerequisite download images need to be self-hosted, not linked to Wikimedia directly.** Jeff tried the tutorial himself and hit a real problem: right-clicking the image displayed on a Wikimedia Commons page and choosing "Save As" grabbed the full master file (14MB in his test), which Joomla then rejected as too large to upload. Explaining Wikimedia's various resolution/download options to the reader would be messy. Agreed with Jeff's proposed fix: self-host a pre-sized copy of each prerequisite image at that tutorial's own `images/articles/NNN/` path (the same media-hosting mechanism used for every screenshot in this project), and have the reader right-click-save that instead — this is also exactly what the original, pre-my-involvement CM4.1 draft was already doing (`images/articles/303/Crab_Nebula.jpg`), which I'd mistakenly "corrected" away earlier in this same session, assuming it was a fabricated path rather than an intentional, not-yet-populated one. Reverted that assumption.

Applied consistently, with one nuance per tutorial:
- **CM4.1 and CM4.3:** both self-host their prerequisite images pre-sized at 720px wide (the standard this project already established in CM4.2's own "Resizing Images" section) — ready to use as-is, no resizing needed by the reader.
- **CM4.2 is the deliberate exception:** its own "Resizing Images" section teaches the reader to shrink an image to 720px using Joomla's Media component — so pre-sizing its prerequisite downloads to 720px would make that lesson pointless (nothing to visibly resize). Its three prerequisite images should stay larger than 720px — big enough that the resize step has real, visible work to do, but well under any reasonable upload limit (nowhere near Jeff's 14MB problem case). Added a Note in the file flagging this is intentional. CM4.2's PDF link is unaffected by any of this — it already points at the real NASA-hosted URL, and PDFs don't have Wikimedia's multi-resolution ambiguity.
- **CM4.3 also needed a real gap fixed**, unrelated to the sizing question: I'd never actually told the reader where to get the Jupiter, Andromeda Galaxy, and Crab Nebula composite images in the first place — the Prerequisites section was simply missing that bullet entirely. Added it.

**New/updated open item:** Jeff needs to prepare and upload nine images total to their respective `images/articles/NNN/` paths before these tutorials are usable: two for CM4.1 (Crab Nebula, Orion Nebula, both 720px), three for CM4.2 (the telescope images, left larger than 720px on purpose), and three for CM4.3 (Jupiter, Andromeda Galaxy, Crab Nebula composite, all 720px) — sourced from the Wikimedia Commons pages already cited in each file's own Attribution section. This is now a prerequisite-asset task alongside the screenshot list, not just a screenshot task.

**Correction: CM4.1's float mechanism confirmed and corrected against Jeff's real testing.** Jeff tried the "Add a Second Image, Floated" section himself and sent screenshots of two real issues:
- **Float mechanism now confirmed accurate.** My original draft used vague, hedged language ("look for an Advanced tab, a Class or Style option") since it hadn't been verified. Jeff's screenshot of the actual Insert/Edit Image dialog showed the real fields: **Width** (with a proportion-lock icon that auto-updates **Height**) and a **Class** dropdown offering No Class Selected / None / Left / Right / Center — selecting Left or Right is what floats the image. Rewrote the two relevant steps with these exact field names.
- **Caption-vs-new-paragraph click corrected.** My original first step said to click at the end of the caption and press Return to start a new paragraph. Jeff found this actually just adds a second line within the caption. Fixed: click the image itself first (revealing the blue bounding box), then click just to the right of that bounding box, then press Return — with a Note explaining the distinction.
- **Float-clearing behaviour noted but deliberately not taught as a step.** Jeff's testing also showed that once an image is floated, every subsequent paragraph keeps wrapping alongside it (normal CSS behaviour) until something clears it — he worked around it himself using a "float-end" class from the toolbar's Container dropdown. He called this "far beyond the scope of this tutorial" while still wanting the basic float shown. Resolution: the tutorial's own script doesn't add any paragraph after the floated image (so the issue doesn't surface within the steps themselves), and Concepts now has one sentence acknowledging a floated image affects everything that follows until something moves past it, without walking through how to solve it.

I initially dropped the border instruction from the second image entirely, on the assumption it wasn't confirmed. Jeff then checked and found it: it lives under the **Advanced** tab of the same *Insert/Edit Image* dialog — **Border width** and **Border style** fields (Solid, Dotted, Dashed, Double, Groove, Ridge, Inset, Outset, None, Hidden), alongside Vertical/Horizontal space. Restored the border step (width 4, style Solid) right after the Class/float step on the Orion Nebula image, restored the h3 title "Add a Second Image, Floated with a Border," and added a Concepts sentence on the Advanced tab's border/spacing fields.

This closes out the earlier "float/border mechanism unconfirmed" open item for CM4.1 — both now confirmed. CM4.3's own Float option (for Intro/Full Article Images, a separate field from this one) remains unconfirmed and open.

### Screenshot recommendations — CM4.1 (images/articles/303/)

1. After creating the Astronomy category — the new-category form or the categories list showing it added.
2. After the Media popup opens from the CMS Content menu.
3. After creating the Astronomy media folder.
4. After uploading and inserting the Crab Nebula image with alt text.
5. After checking Show caption and typing the caption.
6. After building the "Notable Objects Nearby" list, showing the Orion Nebula thumbnail inline within the second list item.
7. After building the table, showing the reused Crab Nebula thumbnail in a cell alongside its fact.
8. The Insert/Edit Image Advanced tab, showing Border width 4 / Border style Double set on the Hubble Space Telescope image.
9. The finished article in Preview, showing all four elements together — captioned image, list with inline image, table with image, and the bordered telescope illustration.

### Screenshot recommendations — CM4.2 (images/articles/304/)

1. The Media component with the images folder and Create New Folder button.
2. The Telescopes folder with its two sub-folders.
3. Dragging an image into Optical Telescopes.
4. The item context menu (ellipsis icon).
5. The image Edit/Resize screen, width set to 720px.
6. The uploaded, renamed PDF in the files area.

### Screenshot recommendations — CM4.3 (images/articles/287/)

1. The Astronomy Articles Blog menu item settings (Category Blog, Category: Astronomy, default options).
2. The frontend category blog page before any images are added.
3. Crab Nebula's Images and Links tab, with Full Article Image and Intro Image set to two different photos.
4. The frontend category blog page after Crab Nebula's intro image is added — showing the composite photo.
5. The Crab Nebula article page itself — showing the different close-up Full Article Image at the top.
6. Jupiter or Andromeda Galaxy's Images and Links tab, showing the same image selected for both Intro and Full Article Image.
7. The Float option on an Intro Image, wherever it turns out to live — this screenshot matters most, since it'll pin down open item #2 above.
8. The finished category blog page with all three articles' intro images visible, including Jupiter's floated one.

**CM3.5: screenshots re-shot, heading reverted, one new fix.** Jeff wanted this tutorial exactly right and retook five of the six images (all but inserting_4_by_4_table.png, which is unchanged from the round above). Re-viewed all six and re-verified against the current text:
- The live article's heading is back to <strong>Plans &amp; Pricing</strong> (ampersand) — reverted the "Plans and Pricing" change from the previous round, since Jeff apparently corrected the article itself back to match the original draft rather than the tutorial needing to match his first typing pass.
- Row 4's last value is <em>Same Day</em> (capital D), not "Same day" as drafted — fixed.
- The "Cmail + calls" typo from the previous round's screenshots is gone — Jeff fixed it on the live site, now reads "Email + calls" everywhere, matching the tutorial text (no text change needed, just confirms it's now consistent).
- All field names/menu paths (Cell properties, Cell type/Header cell, Border width/style, Table properties) reconfirmed unchanged from the previous round.
- Updated all five changed images' width/height attributes to match their new dimensions.
- **Resolved:** Jeff retook inserting_4_by_4_table.png too — now shows "Plans &amp; Pricing" in the background, consistent with the rest. Updated its width/height (945×600 → 929×593). All six CM3.5 screenshots are now fully consistent with each other and with the tutorial text — no open items remain.

**CM4.1: floating dropped entirely; replaced with three lower-risk image demonstrations.** Jeff tried the floated/bordered second image himself and hit a real dead end: adding a caption to a floated image skewed the surrounding markup badly, and there's no reliable, no-HTML way to clear a float afterward — Bootstrap (which backs the editor's Container dropdown) only offers `clearfix` for a *parent* containing floated children, not a utility for clearing a *later sibling*; the `float-end` trick Jeff tried earlier only appeared to work because two right-floated elements happened not to fit side by side, which isn't reliable across templates/widths. Confirmed via web search (Bootstrap's own docs, plus an open GitHub issue asking for exactly this feature). Given that, and that Jeff wasn't willing to ship a tutorial that raises an obvious question ("why does my paragraph still wrap oddly?") without a real answer, we dropped floating from CM4.1 entirely — removed the "Add a Second Image, Floated with a Border" section and all float/border Concepts references.

To keep the tutorial just as interesting (and to avoid wasting the Orion Nebula prerequisite image, which was left unused by the above), added three new demonstrations after the captioned Crab Nebula image, each showing a different place an image can live, none involving floats:
- **Add an Image to a List Item** — a "Notable Objects Nearby" bulleted list where one item embeds the Orion Nebula image inline alongside its text, cross-linking to 3.3 Lists.
- **Add an Image to a Table Cell** — a small 2×2 table reusing the already-uploaded Crab Nebula image alongside a fact, cross-linking to 3.5 Tables, framed explicitly around Jeff's own point that tables are for structured data, not layout — this is a legitimate use, not layout abuse.
- **Add a Bordered Image** — border is revisited here (Advanced tab, Border width/style, confirmed real), but on a new third image instead of a floated one, avoiding the broken combination entirely. Jeff pointed out Joomla's border colour is fixed to black, so it disappears against the dark-background astrophotos — the fix is choosing a light-background image instead. Border style set to Double per Jeff's own finding that Double "kind of works" against the black-border limitation.

Prerequisites now lists three images. The article now also ends with an explicit Save & Close step, which the previous (post-float-removal) draft was missing.

**Correction: replaced the third (bordered) image again — Star Life Cycle Chart didn't work out.** Jeff checked it himself the next morning: it actually has a dark background (doesn't solve the border-visibility problem at all) and loses legibility when resized down to article width. He found a real replacement himself: <a href="https://commons.wikimedia.org/wiki/File:The_Hubble_Space_Telescope_and_the_Faint_Object_Spectrograph_(heic0112a).tiff">The Hubble Space Telescope and the Faint Object Spectrograph</a> (heic0112a) — an ESA/Hubble illustration of the telescope itself with a white background, and Jeff noted it doubles as a nice narrative close: the Orion Nebula photo used earlier in the article was itself captured by Hubble, so the tutorial now ends by showing the reader the instrument that took it. I couldn't render the Commons page directly (fetch returned empty; Claude in Chrome wasn't connected this session either), so I corroborated the credit via web search against ESA's own hubble site — image is officially credited to ESA & the Space Telescope-European Coordinating Facility (ST-ECF), which is what's now in Attribution, rather than assuming "public domain" as Jeff first guessed from the Commons page (ESA/Hubble imagery is typically CC BY 4.0 with required attribution, not PD — doesn't change our workflow since we credit everything regardless, but worth using the accurate credit line). Updated the Prerequisites image, the "Add a Bordered Image" lead-in text (now ties back to the Orion Nebula/Hubble connection instead of "life cycle of a star"), and the Attribution entry. Source file on Commons is a .tiff; Jeff will need to convert to .jpg as part of resizing to 720px, consistent with how every other prerequisite image in this project is handled.

**Updated open item:** Jeff now needs to prepare and upload ten images total: three for CM4.1 (Crab Nebula, Orion Nebula, the Hubble Space Telescope illustration, all 720px), three for CM4.2 (unchanged), three for CM4.3 (unchanged), plus CM4.3's own separate Float option for Intro/Full Article Images remains unconfirmed and open (that field is not part of TinyMCE/Bootstrap and may not share the same clearing problem, but hasn't been tested).

**CM4.1: real images and all nine screenshots placed; full editing pass from Jeff's own notes.** Jeff prepared and uploaded the three real prerequisite images (Crab_Nebula.jpg, Orion_Nebula_(Hubble_Space_Telescope).jpg, The_Hubble_Space_Telescope_and_the_Faint_Object_Spectrograph_(heic0112a).jpg — converted from the Commons .tiff as expected) plus all nine planned screenshots, and sent a detailed set of edits after walking through the tutorial himself:
- **Introduction** simplified to Jeff's own wording, dropping the "with a caption"/"with a border" detail from the opening sentence.
- **Prerequisites** now links to 3.3 Lists and 3.5 Tables (both used later in the tutorial), and the three `<img>` tags now point at the real files with real proportional dimensions (240 wide, heights computed from actual pixel dimensions: 240×240, 240×259, 240×186).
- **Embed an Image with a Caption:** the real workflow uploads all three images at once at the "add to folder" step, then each later step *selects* an already-uploaded thumbnail via its checkbox rather than uploading again — reworded every image-insertion step across the whole article to match (list item, table, and bordered-image sections all now say "tick the checkbox... to select it" instead of "upload"). Added a Note that a size popup appears while dragging a resize handle, and a target of ~600px wide.
- **Add an Image to a List Item:** step 1 reworded to Jeff's exact real-world technique (click image → click right of bounding box or press right-arrow → Return). The Orion Nebula list item is built differently than drafted: type the full line first, Shift+Return twice, insert the image, Shift+Return once, then a hard Return to start a new bullet — closing the list with a third item, *Pleiades Cluster*, that I wrote text for per Jeff's request. Also added a final resize step (right-click image, Width 480, Tab) since the inserted image was too large for the list.
- **Add an Image to a Table Cell:** added the quick toolbar reminder for inserting a 2×2 table, a new step resizing the inserted image to 240px wide so it fits the cell, and replaced the vague header-row instruction with the exact menu path already established in 3.5 Tables (highlight cells → right-click → Cell → Cell properties → Cell type: Header cell).
- All nine screenshots placed at their corresponding steps as `<figure>`/`<figcaption>` pairs, matching the markup convention used throughout the project (e.g. CM3.5), with real pixel dimensions read from each file. Note one filename mismatch from Jeff's list: he referred to the final preview screenshot as "image_article_preview.png" but the actual file on disk is `preview_image_article.png` — used the real filename.

CM4.1 is now fully real: real prerequisite images, real screenshots, no open items remain on this tutorial except the still-outstanding CM4.3 Float-option confirmation (unrelated, separate file).

**CM4.1: Jeff renamed images after Joomla stripped parentheses on upload; checked his edits.** Joomla's Media component removed the parentheses from Orion_Nebula_(Hubble_Space_Telescope).jpg and The_Hubble_Space_Telescope_and_the_Faint_Object_Spectrograph_(heic0112a).jpg when drag-and-dropped in. Jeff renamed the real files to match (no parens) and updated the `src` attributes himself, plus made several of his own wording edits after walking through the tutorial again. Checked the whole file against the real files on disk:
- **Fixed:** the `data-path` attributes on both renamed images still had the old parenthesised names (Jeff updated `src` but not `data-path`) — updated both to match.
- **Fixed:** inserting_crab_nebula_with_alt_text.png was re-taken/edited (now 1280×912, was 1287×984) but the width/height attributes hadn't been updated — fixed.
- All other screenshot dimensions, and the Attribution links (which correctly still point at the real Commons URLs with parentheses — those are external and unaffected by the local rename), checked and correct.
- Jeff's own content edits all read as real improvements from his testing: added the missing alt-text step when reusing the Crab Nebula image in the table, added an explicit "Click Save" after resizing the list's Orion Nebula image, tightened several phrasings.

**Resolved:** the "click the image, click just right of the bounding box, press Return" step was an accidental drop, not deliberate — Jeff confirmed and asked to restore it. Added back as the first step of "Add an Image to a List Item."

**Resolved:** the inline border on the third Prerequisites image was intentional — Jeff added it deliberately, both because he thought it looked better and because it helps define the image's right-click area against the page background. No change needed.
