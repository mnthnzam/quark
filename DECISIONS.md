# DECISIONS — quark

Append-only, newest at top. Bodies are never edited; the only change to a past entry is a status line at its top. No entry without a real rejected alternative. Tags: `[stack] [data] [auth] [ui] [infra] [process] [scope]`.

## 2026-09-21 [ui] — Homepage release slide uses QuarkXPress imagery, not the company hero's
**Context:** Today's homepage hero is company-level: Quark logo, two people with laptops, three products in the copy. The release slide becomes slide 1 of a two-slide slider.
**Chose:** Slide 1 carries the QuarkXPress logo and the product page's model, so it reads as QuarkXPress at a glance. Today's hero becomes slide 2, unchanged.
**Rejected:** Keeping the company imagery — the slide would look like today's hero with new words. Leaving an empty slot for Quark's key visual — nobody has said one is coming.
**Revisit if:** Quark supplies release key art.
**Where:** Figma frame B (node 3:67)

## 2026-09-21 [ui] — Product page shows three new features and three carried over
**Context:** The page has six feature rows today. The size of the new release's feature list is unknown.
**Chose:** Rows 1–3 are new-release features, rows 4–6 the strongest current ones. Which three survive is Andrew's call once the list lands.
**Rejected:** All six rows new — only works if the release has six features each worth a row, and nothing says it does.
**Revisit if:** Bogdan's list has six or more headline features.
**Where:** Figma frame A (node 3:97)

## 2026-09-21 [ui] — The release message sits in an eyebrow row; the product page H1 does not change
**Context:** The H1 "QuarkXPress Desktop Publishing and Page Layout Software" is the page's search line. The release still has to be visible above the fold.
**Chose:** A NEW pill, one release line and a what's-new link above the logo, plus the year badge on the logo.
**Rejected:** Rewriting the H1 as the release headline — louder, but puts the page's ranking at risk and has to be reverted in months. A full-width release band under the header — no SEO cost, but a new pattern the site does not have, against the no-redesign decision.
**Revisit if:** Andrew finds the eyebrow too quiet once real copy is in it.
**Where:** Figma frame A (node 3:74)

## 2026-09-21 [process] — Git runs in terminal mode here
**Context:** Sessions reach this folder through a sandboxed shell on Manthan's Mac. It cannot delete git lock files and holds no SSH key, and the remote is SSH.
**Chose:** `zamstars.mode = terminal`. The agent hands over fenced git blocks and waits for the output.
**Rejected:** `direct` — commits would work through a lock-parking helper as in the CISCO repo, but every push would still need a human, so the mode would be half-true.
**Revisit if:** the remote moves to HTTPS with a credential the sandbox can use.

## 2026-09-21 [infra] — Quark lives in its own private repo
**Context:** The zamstars pre-flight showed a handoff would push Quark material — a site security finding and a Crossover-internal call transcript — into `mnthnzam/CISCO`, another client's repo.
**Chose:** New private repo `mnthnzam/quark`; folder moved out of CISCO; a one-line pointer stays behind.
**Rejected:** Operating layer in place inside the CISCO repo — puts one client's material in another client's history for good. In place but gitignored — nothing leaks, but nothing is pushed, which breaks the rule that uncommitted work does not exist.
**Revisit if:** Zamstars moves all client ops into a single private monorepo.
**Where:** this repo

## 2026-09-21 [infra] — Quark work sits in `quark/` inside the CISCO folder
> SUPERSEDED 2026-09-21 by Quark lives in its own private repo
**Context:** Project opened mid-session from a Cisco workspace; Manthan asked for a side project inside that project.
**Chose:** Self-contained `quark/` subfolder with an isolation note, one-line pointers in the CISCO index.
**Rejected:** A separate project from the start — flagged as the cleaner option, deferred for speed on day one.
**Revisit if:** the work outlives October, or anything needs pushing.

## 2026-09-21 [ui] — Design shells are cloned from the captured live pages, not redrawn
**Context:** The Figma file is an HTML capture of quark.com — absolute layout, no components, styles or variables. Andrew's brief: a new version of what is already there.
**Chose:** Clone the live hero, feature and homepage sections into one new Figma section and edit the copies. Originals untouched.
**Rejected:** Building shells before seeing the live pages — any shell would be a guess at their system. Redrawing as a fresh component set — overshoots the brief and costs days we don't have.
**Revisit if:** Quark supplies a real design system or component library.
**Where:** Figma `w7KtCUEKUuXt2mlkhzg8SL`, section node 3:2 · `design/DESIGN-NOTES.md`

## 2026-09-21 [process] — One master announcement email; every variant is cloned from it
**Context:** The old team hand-built each release email. Andrew now has AI for HTML and a handful of part-time people.
**Chose:** Design delivers one finished email. Andrew clones the audience variants from it. Only the intro block and the audience block differ between variants.
**Rejected:** Designing each audience's email separately, as before — not feasible in nine days.
**Revisit if:** Pardot shows an audience whose email cannot be expressed as a variant of the master.
**Where:** Figma frame C (node 5:2)

## 2026-09-21 [scope] — One landing page with parameter-driven variants
> PROPOSED 2026-09-21 by Andrew
**Context:** The old team kept a dedicated landing page per campaign, probably to feed remarketing audiences. Remarketing is assumed to be going ahead.
**Chose:** Aim for a single page, with audiences separated by UTM or parameter.
**Rejected:** One page per audience — around eleven pages to maintain, "really impractical".
**Revisit if:** Andrew's Pardot scoping shows audiences whose offer or price cannot share a page.

## 2026-09-21 [infra] — Cleverbridge lifecycle emails stay in Cleverbridge
**Context:** Cleverbridge is the payment provider and also sends every automated email — trial started, download, renewal, last day of trial.
**Chose:** Leave them there. Quark's side (Bogdan, Ivan) updates them; we supply assets if asked.
**Rejected:** Migrating them into Customer.io — a separate, much larger job, and they run today with no action from us.
**Revisit if:** Quark asks us to edit or own any Cleverbridge email.

## 2026-09-21 [scope] — Infografix: menu links come out now, the pages stay
**Context:** Quark sunset Infografix without notice; `infografix.app` redirects to quark.com. It is still linked in the header, footer, a homepage block and the product page add-ons.
**Chose:** Remove the links. Keep the pages.
**Rejected:** Deleting the pages — infographic features may be folded into the new release, and the content could feed the release story or a sunset email.
**Revisit if:** Bogdan confirms no Infografix capability is in the new release.

## 2026-09-21 [scope] — No video per feature
**Context:** The product page carries six feature videos and the what's-new page seven. Nobody on this team makes product videos.
**Chose:** New features get a UI screenshot in the existing device mock-up. At most one release video, from Arjun. Play buttons hidden in the shells.
**Rejected:** A video for every feature, as today — "over the top" and not producible in the time.
**Revisit if:** Quark's product team delivers feature videos unprompted.

## 2026-09-21 [scope] — New versions of what exists, inside existing templates; no redesign
**Context:** Roughly nine days, hundreds of touchpoints, a part-time team. Andrew: "I'd rather have the new version of what's there than have you overshoot."
**Chose:** Homepage slide, product page and email are updated versions of the current patterns. Substance — words, message — over looks.
**Rejected:** Pushing the design forward the way we do on Crossover — risks missing the things that have to happen.
**Revisit if:** the release slips by two weeks or more.

## 2026-09-21 [scope] — We do not replicate the old team's output
**Context:** The previous marketing team was about a dozen people taking about four months per release.
**Chose:** Cut, merge or switch off pages, videos and landing pages. Proposals go on the audit's orange and red lists; nothing is deleted unilaterally.
**Rejected:** Keeping every existing page current — "if we try… we will fail".
**Revisit if:** Quark staffs a marketing team again.

## 2026-09-21 [process] — The audit is a traffic-light Google Sheet, merged with Carla's
**Context:** Nobody will hand us a change list at useful granularity; Carla is auditing the site in parallel.
**Chose:** One row per change. Green = trivial · yellow = needs master assets · orange = probably remove, needs a conversation · red = no-brainer delete. One merged source of truth.
**Rejected:** A Word document — Andrew asked for a sheet, explicitly. Waiting for Quark to supply the list — it will not arrive at this level of detail.
**Revisit if:** Carla's list turns out to use a different structure we should adopt instead.
**Where:** `audit/site-audit.csv`
