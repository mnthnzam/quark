# quark

Zamstars' working repo for the **QuarkXPress release**, target Wed 30 Sep 2026. Not an app — a marketing-ops project: site audit, design shells, email, landing pages, remarketing. Client chain: Quark Software ← Andrew Allen ← Zamstars. Opened 21 Sep 2026, expected life 2–3 weeks.

Owner: Manthan Gohil. Working with: Vinodh Talapaneni (site, GTM, Ads, forms), Harisankar V (design).

## What's here

| Path | Answers |
|---|---|
| `STATE.md` | What is true right now — in flight, broken, next, open questions. 12 bullets max. |
| `DECISIONS.md` | Why things are the way they are, and what was rejected. |
| `docs/LEDGER.md` | What left STATE, when and why. |
| `docs/CONTEXT.md` | People, systems, timeline, how Andrew wants this run. The stable picture. |
| `docs/WORKLIST.md` | The full backlog — every piece of Quark work, by workstream, owner, blocker. STATE is the top of this. |
| `docs/QUESTIONS.md` | Every open question and who can answer it. |
| `audit/site-audit.csv` | Traffic-light site audit, one row per change. Import to Google Sheets. `urls_raw.txt` = 649-URL site map. |
| `design/` | Figma node map, tokens read from the live site, previews of the shells (v2 = after the 21 Sep design calls). |
| `sources/` | Raw inputs, date-prefixed, never edited after landing. |
| `docs/LOG-2026-09-21.md` | Frozen record of day one, before this operating layer existed. |

## How to run it

Nothing to build or install. Start a session with **catchup**, end with **handoff**, say **decision** the moment a real choice is made. Git is in **terminal mode**: the agent hands you git blocks, you run them and paste the output back.

New inputs — Bogdan's messaging, Andrew's Pardot export, email HTML — go in `sources/` as `YYYY-MM-DD_<what>.<ext>`.

Provenance tags used in `docs/` and the audit: `call` = said on the 21 Sep call · `scan` / `scan2` = read from quark.com on 21 Sep, text only, no visual check · `map` = from the URL map · `inf` = inferred, verify before acting.

## Where it runs

Nowhere — no deploy. The work lands in other people's systems:

| System | Used for | Who holds access |
|---|---|---|
| quark.com (WordPress, WPML, 7 languages) | every site change | Vinodh |
| Figma `w7KtCUEKUuXt2mlkhzg8SL` | design shells | Manthan, Hari |
| Pardot via Salesforce | release emails, audiences | Andrew — shared renewal-team login + shared authenticator |
| Cleverbridge | checkout, renewals, lifecycle emails | Quark (Bogdan, Ivan) |
| content.quark.com | gated PDFs and forms the site can't edit | unknown — open question |
| GTM + Google Ads | remarketing | Vinodh |
| Proxi.id | academic, charity and government eligibility checks before purchase | unknown |
| GitHub `mnthnzam/quark` | this repo | Manthan |

No credentials belong in this repo. There is no `.env`; if one ever appears it is already gitignored.

## Depends on

Two inputs gate most of the work: **release messaging from Bogdan** (name, version, features, message) and **Andrew's Pardot scoping** (templates, HTML, audiences). `docs/WORKLIST.md` marks them `MSG` and `PARDOT`.
