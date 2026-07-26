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
