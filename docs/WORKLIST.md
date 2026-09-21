# QUARK — worklist

Every piece of Quark work surfaced on the 21 Sep call, plus what the same-day site scan added. Status as of 21 Sep 2026, end of session 2 (audit pass 2 + Figma shells v1).

**Status:** `open` · `doing` · `blocked` · `done` · `dropped`  **Blockers:** `MSG` = release messaging from Bogdan · `PARDOT` = Andrew's Pardot scoping (22 Sep)

Source column: `call` = 21 Sep transcript · `scan` = quark.com scan 21 Sep · `inf` = inferred, verify.

---

## A. Manthan + Hari — design (the direct ask)

Brief: homepage slider, main product page, announcement email. Shell now, fill when messaging lands. Stay inside existing templates. Substance over polish. See DECISIONS.md.

| ID | Work | Owner | Status | Blocked by | Src |
|---|---|---|---|---|---|
| A-01 | **Announcement email — shell.** Component structure from what's knowable today (brand, prior release pattern). One finished email within 1–2 days of receiving messaging + last release's HTML; Andrew clones the rest with AI. | Manthan, Hari | **shell v1 in Figma** (frame C) | MSG + PARDOT (finish) | call |
| A-02 | **QuarkXPress product page — hero + feature section.** Updated version of `/products/quarkxpress`. Six feature blocks today, each with a video. | Manthan, Hari | **shell v1 in Figma** (frame A) | MSG (finish) | call |
| A-03 | **Homepage slider / hero** for the release. Today's hero is static + company-level; shell = slide 1 of a 2-slide slider. | Manthan, Hari | **shell v1 in Figma** (frame B) | MSG (finish) | call |
| A-04 | **Feature visuals plan.** For each new feature: what do we show? Output = a specific screenshot request list for Quark's product team ("we need screenshots of these five things"). | Manthan, Hari | blocked | MSG | call |
| A-05 | **Video position.** Recommend: keep / drop the "Watch video" button; per-feature videos (Andrew: over the top, not needed) vs one ~1-min video (Arjun). | Manthan → Andrew | open | — | call |
| A-06 | Pull current site patterns as design starting point: hero, feature block, slider, existing email templates (latter via Andrew). | Manthan | done — Figma file `w7KtCUEKUuXt2mlkhzg8SL` is a capture of the live pages; no components, styles or variables in it. Tokens in `design/DESIGN-NOTES.md` | — | inf |

## B. Website audit + updates — Carla captain, Zamstars builds the granular list

| ID | Work | Owner | Status | Blocked by | Src |
|---|---|---|---|---|---|
| B-01 | **Granular traffic-light audit in a Google Sheet** — page, item, change, type, light. File: `audit/site-audit.csv`. Could be driven through the WordPress MCP connector. | Zamstars (unassigned) | doing — 68 rows in `audit/site-audit.csv`, ~45 pages read | — | call |
| B-02 | Merge Zamstars' list with Carla's into one source of truth. | Carla + Zamstars | open | B-01 | call |
| B-03 | **Green sweep**: year/version swaps across pages, menus, buttons, PDF links. Only after the release name is known. | Vinodh | blocked | MSG (name) | call |
| B-04 | Flagship updates: homepage, `/products/quarkxpress`, What's-new page. Implements A-02/A-03. | Vinodh + design | blocked | MSG | call |
| B-05 | What's-new page: add the new version block above the v22.0.1 block (page is a running changelog back to v20). New "What's New" PDF on content.quark.com — owner unknown. | Vinodh | blocked | MSG | scan |
| B-06 | **Reviews module**: reported broken/outdated. Product page embeds four Gartner snippet iframes + a Capterra logo; homepage links G2. Decide fix / re-source / drop. Can happen now. | Vinodh → Andrew | open — **confirmed broken**: the Figma capture of the page shows a DNS error where each Gartner embed should be | — | call+scan |
| B-07 | **Remove Infografix link** from header + footer menu. Pages stay (see DECISIONS). | Vinodh | doing (due 21 Sep) | — | call |
| B-08 | Infografix — remaining mentions: homepage block ("get started" → infografix.app), product page add-ons section, anything else. Find and decide per DECISIONS. | Zamstars | open | — | scan |
| B-09 | Orange/red list: pages to retire or merge. Propose, don't delete. | Zamstars → Andrew/Carla | open | B-01 | call |
| B-10 | Partner network pages — Vinodh did content updates; layout inconsistent (some entries have descriptions, some don't). Functional. Low priority. | Vinodh | done (content) / open (format) | — | call |
| B-11 | System requirements block on product page (macOS / Windows versions) — will need the new release's requirements. | Vinodh | blocked | MSG | scan |
| B-12 | Stale campaign tags: shop buy-buttons carry `x-campaign=26AprilPromo`. Check whether it's cosmetic or drives pricing at Cleverbridge. | Vinodh | open | — | scan |
| B-13 | Dated awards strip on homepage (2023 / 2023–24 / 2024 badges). Orange candidate. | Zamstars → Andrew | open | — | scan |
| B-14 | **Language versions**: switcher lists ~40 languages. Establish whether auto-translated (then free) or hand-maintained (then scope multiplies). | Vinodh → Andrew | **answered**: WPML, 7 hand-translated languages (en, de, es, fr, it, ja, ko). The ~40-language switcher is a separate overlay. Decision needed: EN-only at launch? | — | scan |
| B-15 | Audit the **email → landing page path** for every email that will send. | Zamstars | blocked | PARDOT | call |
| B-16 | **SECURITY — `/academic` carries 9 hidden outbound links to unrelated sites** (SEO link injection). Verified by live link extraction; absent on 39 other pages incl. `/de/academic`. Remove, check page revisions (modified 2025-10-20), rotate that editor's password, run a malware scan. | Vinodh | **open — do first** | — | scan2 |
| B-17 | Installers page: new Recommended tile + files at launch; 8 existing labelling/UTM defects to fix in the same pass. Launch-day critical. | Vinodh + Quark product team | blocked | installer files | scan2 |
| B-18 | Documentation: new version tile + cloned version page; current 2026 page links to 2019/2021/2023 docs. | Vinodh + Quark docs | blocked | docs from Quark | scan2 |
| B-19 | **Release comms nobody mentioned**: every past release had a press release on `/about/news` and 1–2 launch posts on `/about/blog`. Who writes these? | Andrew | open | MSG | map |
| B-20 | Red list, ready to action: `/quarkxpress-webinar-series` (Oct 2021, live Zoom links), `/qxpcontest` (2023). Orange: `/choose-how-you-buy-complete` (2024 copy), CopyDesk page. | Vinodh → Andrew | open | Andrew OK | scan2 |
| B-21 | One shared "QuarkXPress 2026 Features" block repeats on 5 capability pages. If it's a reusable block: one edit. Check in WP. | Vinodh | open | — | scan2 |
| B-22 | Fix-now greens, no dependency: trial page meta description says "QuarkXPress 2021"; `/ai-in-quarkxpress` says "2026 (v21.1)"; `/request-previous-version` dropdown stops at 2024; legacy `quarkportal.force.com` KB links; malformed affiliate URL. | Vinodh | open | — | scan2 |

## C. Email — Andrew captain

| ID | Work | Owner | Status | Blocked by | Src |
|---|---|---|---|---|---|
| C-01 | Scope Pardot: last release's templates, HTML, audience criteria, send counts. Traffic-light which emails repeat. | Andrew | doing (22 Sep) | — | call |
| C-02 | Check audience criteria still resolve — expect attributes nobody has regenerated in ~6 months. Worst case: ticket Quark to rebuild segments. | Andrew (+Vinodh) | open | C-01 | call |
| C-03 | Verify Salesforce → Pardot sync. | Vinodh | open | Pardot login | call |
| C-04 | Pardot access for Vinodh — shared login or a proper marketing login. | Andrew | open | — | call |
| C-05 | Master announcement email (= A-01), then AI-cloned variants per audience. | Andrew + design | blocked | A-01, MSG | call |
| C-06 | Upgrade-offer emails for end-of-life version holders — find them, find the page + pricing they point at. | Andrew | open | C-01 | call |
| C-07 | Possible Infografix sunset email to its users; possible "infographics now inside QuarkXPress" angle. Idea only. | Andrew | open | MSG | call |
| C-08 | Cleverbridge automated emails — Quark side (Bogdan → Ivan) owns. We may supply assets. | Quark | open | — | call |

## D. Landing pages, forms, commerce — Vinodh

| ID | Work | Owner | Status | Blocked by | Src |
|---|---|---|---|---|---|
| D-01 | Inventory existing campaign landing pages (old team kept one per campaign, likely to feed remarketing audiences). | Vinodh | open | PARDOT helps | call |
| D-02 | Design the simpler model: **one landing page, variants by UTM/parameter** rather than ~11 pages. Confirm it still supports per-audience remarketing. | Vinodh + Andrew | open | C-01 | call |
| D-03 | **Find the upgrade form / upgrade purchase path.** Nobody knows where it lives. Renewals page just hands off to Cleverbridge; shop shows no upgrade SKU. `/solutions/quarkxpress-support-hub` is the only page that explains it: upgrades = maintenance contract, via Cleverbridge or qxpsales@quark.com. `/pinterest-campaign` is the only live discount LP (10% / 20% off). | Vinodh | open | C-06 helps | call+scan |
| D-04 | Forms inventory. Known: "Request a call" modal (site-wide), whitepaper gate, forms on content.quark.com that WordPress can't edit. Who owns content.quark.com? | Vinodh | open | — | call+scan |
| D-05 | **Currencies**: five exist. How are they served — geo-IP, switcher, separate pages? Scan saw no prices or currency control in page text (probably JS / Cleverbridge-side). Simplify if possible. | Vinodh | open — **partly answered**: prices render in the visitor's currency on one URL (the Figma capture shows ₹). So geo-IP, not separate pages. Mechanism (Cleverbridge script?) unconfirmed | — | call+scan |

## E. Paid remarketing — assume it's happening

| ID | Work | Owner | Status | Blocked by | Src |
|---|---|---|---|---|---|
| E-01 | **Readiness check**: Google Ads access, GTM container live on site, remarketing tag firing, audience lists populating, consent setup. Find blockers now. | Vinodh | open | — | call |
| E-02 | Audience structure: minimum two messages — *buy* vs *upgrade your unsupported version*. Fewer is better. | Andrew | blocked | C-01 | call |
| E-03 | Ad creative from the master features-and-benefits list. | design + Arjun | blocked | MSG | call |
| E-04 | Social remarketing to the same lists, creative from Arjun. Maybe. | Arjun | open | MSG | call |

## F. Master assets — write once, fold out

| ID | Asset | Owner | Status | Blocked by |
|---|---|---|---|---|
| F-01 | Master features-and-benefits list | Andrew (+us) | blocked | MSG |
| F-02 | Master announcement email | design + Andrew | blocked | A-01, MSG |
| F-03 | Master visual set: hero, per-feature images | design | blocked | MSG, screenshots |
| F-04 | ~1-min release video | Arjun | open (unconfirmed) | MSG |

## G. Not ours / parked

- Quark Layout — no action.
- QPP, Docurated, CopyDesk, Server pages — untouched unless they name the QXP version.
- Careers page — Andrew already repointed some roles to Crossover.
- Customer.io migration of Cleverbridge emails — explicitly not happening.

---

## What can move now, with nothing from Quark

**B-16 (security) first.** Then B-22 · B-06 · B-07 · B-08 · B-20 · B-21 · B-12 · D-04 · E-01 · A-05. Design shells A-01/02/03 are at v1 and wait on MSG.
