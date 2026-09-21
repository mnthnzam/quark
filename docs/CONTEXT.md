# QUARK — context

Last updated: 21 Sep 2026 (opening state, from the 21 Sep weekly call + a same-day scan of quark.com).

## 1. The situation in five lines

- Quark is shipping a new QuarkXPress release. They want it out "by end of September". Andrew has told them he reads that as **exactly 30 Sep, not earlier**. `[call]`
- Andrew set Quark a deadline of **Mon 21 Sep** to answer his open questions and hand over *what the release is* — features, message. Quark (Bogdan) said they'd try to meet it. When that lands, a 9-day clock starts. `[call]`
- The old Quark marketing team was ~12 people and took ~4 months per release. Now it is Andrew, Carla, Arjun and Zamstars, part-time. `[call]`
- Quark is a recent acquisition; Andrew has "no more context than you have". Decisions a client would normally make fall to us. `[call]`
- **Quark outranks Crossover for the next ~2 weeks.** Crossover tasks fall in line behind it. `[call]`

## 2. What failure looks like (Andrew's words, condensed) `[call]`

1. Quark hits their date and **we block the deployment** — emails can't send, lists can't populate, key pages not updated. Not acceptable.
2. We launch on time but with **predictable stuff-ups** — an email points to a page that's broken, wrong or still says last year. Audit the path, email → landing page.
3. Acceptable: minor pages still being tweaked after launch.

Dates are soft in both directions: Quark might say "Thursday", or reach the 30th and need two more weeks.

## 3. People

| Who | Side | Role here |
|---|---|---|
| Andrew Allen | Crossover / Quark marketing | Runs it. **Captain of email.** Decides escalations. |
| Carla | Andrew's side | **Captain of website** — what lives where. Running her own page audit; lists get merged. |
| Arjun | Andrew's side | Organic social. Candidate for a ~1-min release video and social remarketing creative. |
| Vinodh Talapaneni | Zamstars | Technical: WordPress, GTM, Google Ads, forms, landing pages. In the Quark thread. |
| Harisankar V (Hari) | Zamstars | Design, with Manthan. |
| Manthan Gohil | Zamstars | Design lead on the three design deliverables. |
| Bogdan | Quark | Source of the release messaging / feature list. |
| Ivan | Quark | Addressed by Bogdan re: Cleverbridge emails. Role unclear. |
| Dragos | Crossover | Andrew's boss. Crossover-side only — Andrew has to tell him Quark is taking the fortnight. |

Transcript spells several names inconsistently (Hari/Hadi/Harry, Dragos/Dragosh/Trago, Quark/Cork/Park). Spellings above are best guesses.

## 4. Systems

| System | What it does | Access / state |
|---|---|---|
| quark.com | WordPress. Marketing site, ~40 language options in the switcher `[scan]`. | Vinodh has WP access. A WordPress MCP connector exists — Andrew suggested using Claude with it for the audit. `[call]` |
| Pardot (Salesforce Marketing Cloud Account Engagement) | Marketing email — announcement emails, audiences, templates from the last release. | Via Salesforce, **shared renewal-team login + shared authenticator**. Andrew confirmed he's in on 21 Sep. May share with Vinodh. Asked Quark for a proper marketing login. `[call]` |
| Salesforce | CRM; site chat routes into it. Pardot syncs from it. | Vinodh suspects the sync may be broken; Andrew thinks it works (active-customer count has moved). Unverified. `[call]` |
| Cleverbridge | Payment provider **and** marketing add-on that sends every automated lifecycle email (trial started, download, renewal, last trial day). `checkout.quark.com` and the renewals page route to it. `[call]` `[scan]` | Quark side (Bogdan → Ivan) is to handle Cleverbridge email updates. We may be asked for assets. Out of our scope unless that changes. |
| content.quark.com | External domain hosting gated PDFs and the forms Vinodh found — **the website has no control over these forms.** `[call]` `[scan]` | Owner unknown. |
| GTM + Google Ads | Needed for remarketing. | Vinodh is in both. Readiness unverified. |
| Customer.io | Crossover's tool. Andrew's stated condition: Cleverbridge emails stay where they are; migrating them to Customer.io would be a different, bigger job. | Not in scope. |
| Nex | Crossover's internal AI/data assistant. Andrew has asked whether Quark can get a version. | Not available for Quark today. |

## 5. The product and the site today `[scan]`

- Current release on site: **QuarkXPress 2026, v22.0.1**. Prior: 2025 v21.1 (May 2025), v21 (Nov 2024), v20 (Nov 2023).
- New release name/number: **unknown.** Andrew said "change 2026 to 2027" as an example, not as fact.
- Licensing: annual subscription or perpetual + 1 yr maintenance. AI features need subscription or active maintenance from v21.1.
- Product page sells six features, each with a YouTube video: Variable Fonts, Mathematical Equations, Quarky AI, Paste Into, Font Pairing, Paper Color Previews. What's-new page lists eight, seven with video.
- Other products on the site: Quark Publishing Platform (QPP), Quark Docurated, CopyDesk, QuarkXPress Server. **Not part of this release** — leave alone unless they mention the QXP version.
- **Infografix**: sunset by Quark with no notice; `infografix.app` now redirects to quark.com. Still linked from header menu, footer, homepage block and the product page add-ons section as of the scan.
- **Quark Layout**: a product that was being prepared (social handles reserved) but never reached the site. No action expected. `[call]`

## 6. How Andrew wants this run `[call]`

- **Traffic-light audit**, in a Google Sheet, granular (page → item → change). Green = trivial (year swap). Yellow = needs real attention, fed from master assets. Orange = probably remove/simplify, needs a conversation. Red = no-brainer delete.
- **Master assets first, then fold out**: one master announcement email, one master features-and-benefits list, etc. Yellow items get populated from these.
- **We do not have to do everything the old team did.** Simplify, merge, switch off. Fewer landing pages, fewer videos.
- **Do the logical thing without asking.** Escalate only real judgment calls. Andrew can't review everything — "we have to move faster than that".
- **Design restraint**: new version of what's already there, inside existing templates. Substance (words, message) over looks. Not a redesign. On Crossover he pushes the boat out; on Quark "the easier it is to just say yes, the better".
- Broken things found now can be fixed or switched off now — no need to wait for messaging.

## 7. Timeline

| Date | What |
|---|---|
| Mon 21 Sep | Briefing call. Quark's deadline to deliver messaging + answers. Vinodh removes Infografix link from header/footer. |
| Tue 22 Sep | Andrew scopes Pardot: templates, HTML, audiences, counts from the last release. Traffic-lights which emails repeat. Expects to report by ~this time. |
| 22–23 Sep | Messaging expected from Bogdan. Unblocks all yellow work. |
| +1–2 days after messaging + last year's HTML arrive | Manthan/Hari deliver one finished announcement email shell. |
| Wed 30 Sep | Target release. Treat as fixed until told otherwise. |

## 8. Known unknowns

Live ones are in `STATE.md` → Open questions; the full list was in the 21 Sep table, now `docs/QUESTIONS.md`. The big ones: release name and feature list; whether the ~40 language versions are auto-translated or hand-maintained; where the upgrade form lives; how the five currencies are served; whether Pardot audiences still resolve.
