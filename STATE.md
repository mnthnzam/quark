# STATE — quark
Updated: 2026-09-21 by Manthan
Active: Manthan (since 2026-09-21)
Branch: main

## In flight — half-done, do not touch without talking to Active
- (09-21) Release shells v1 in Figma: product page, homepage slide, email — every line of copy is a bracketed placeholder; fill when Bogdan's messaging lands
- (09-21) Site audit, 71 rows, `audit/site-audit.csv` = Google Sheet https://docs.google.com/spreadsheets/d/1C9wkk5t55XFJPWsmYc2fTl4fvRh9o7mWZFUqu1Rd-rw — 18 rows checked against the live pages (column `Verified live`), the other 53 still unchecked; not shared with anyone, not merged with Carla's list
- (09-21) Andrew scoping Pardot (last release's templates, HTML, audiences), due 09-22 — the email shell must be reconciled with what he finds
## Broken / risky — known bad right now
- (09-21) quark.com/academic carries 9 injected spam links, still live at 17:15 IST 21 Sep → compromised editor account or plugin; Vinodh: remove, check page revisions, rotate password, scan
- (09-21) Gartner review embeds on the product and trial pages: host does not resolve from two networks, so dead for every visitor → `/request-previous-version` already shows Capterra 2025 quotes as plain text (QA-070); reuse that block, Andrew's call (Q-07)
- (09-21) Don't touch: Figma sections "Home Page" and "Quark Xpress Product" — captures of the live site; clone from them, never edit them
## Next up — safe to pick up cold
- (09-21) Fix-now greens, `docs/WORKLIST.md` B-22 — five site edits with no dependency on Quark
- (09-21) Share the audit Sheet with Carla and Andrew — it sits in Manthan's Drive, shared with nobody; `audit/site-audit.xlsx` is the same data with colour fills (File → Import → Replace spreadsheet)
- (09-21) Video recommendation for Andrew, A-05 — keep or drop "Watch video"; the shells currently hide it
## Open questions — best place to pitch in
- (09-21) Release name, version, features, message? Bogdan, was due 09-21 — unblocks every yellow audit row and all three shells
- (09-21) Translations at launch: English only, or all 7 WPML languages? — decides whether the audit is ×1 or ×7
- (09-21) Who writes the press release and launch blog post? — every past release had both and nobody has raised it
