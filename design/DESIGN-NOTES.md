# QUARK — design notes

## Figma

- File: https://www.figma.com/design/w7KtCUEKUuXt2mlkhzg8SL/Quark-Website-x-Product (single page, "Page 1")
- Source sections (captures of the live site, **do not edit**): `Home Page` 1:1599 · `Quark Xpress Product` 1:2096
- Working section: **"Release shells — 21 Sep"** — node 3:2
  - A · Product page release version — 3:3 (hero 3:74, features 3:97)
  - B · Homepage release slide — 3:67 (hero 3:137)
  - C · Announcement email master shell, 600px — 5:2
  - READ ME note — 5:49

The file has no components, text styles, paint styles or variables. It is an HTML-to-Figma capture: absolute positioning, DOM-style layer names. Work by cloning sections, not by looking for a design system.

**Trap:** captured nodes carry scale constraints. Size the destination frame first (`resizeWithoutConstraints`), then clone into it. Resizing a parent after cloning distorts every child.

## Tokens read from the captures

| Token | Value | Where |
|---|---|---|
| Brand pink | `#FC2A57` (also `#FC2A51` on text) | buttons, feature headlines, links |
| Ink | `#222222` / `#000000` | headings, body |
| Grey | `#777777`, `#8F8F8F`, `#ABABAB` | secondary text |
| Surfaces | `#FFFFFF`, `#F5F5F5`, `#F2F2F2`, border `#DDDDDD` | |
| Product accents | QPP green `#75CF00` · Docurated magenta `#CF00B9` | homepage inline links |
| Body | Roboto Regular 15 / ~25 line height | |
| Product page H1 | Roboto SemiBold 32 | |
| Homepage H1 | Roboto Slab SemiBold 38 | |
| Section H2 | Roboto SemiBold 35 | |
| Feature headline | Roboto SemiBold ~16–20, pink | |
| Buttons | Poppins Bold 12, uppercase, ~2px tracking, radius 4; solid pink or white with pink outline | |
| Attribution | Roboto Condensed Bold Italic 15 | |

## What was changed in each shell, and why

**A · Product page**
- H1 untouched — it is the page's SEO line. Release message sits in an eyebrow row above the logo (`NEW` pill + one line + "See what's new →").
- Year badge on the logo covered with a `20XX` placeholder pill. The real logo is one image; Quark must supply the new brandmark.
- Hero quote (Martin Turner) names QuarkXPress 2026 → replaced by a labelled slot.
- Feature rows 1–3 → new-release slots with "screenshot slot" chips. Rows 4–6 keep today's copy as carried-over features. Which three survive is open (open).
- Six per-feature play buttons and the "Watch video" button are hidden (visible = false), not deleted (no video per feature — see DECISIONS).
- CTA reads "See everything new in QuarkXPress 20XX".

**B · Homepage**
- Today's hero is static and company-level (three products). Shell = slide 1 of a two-slide slider; today's hero becomes slide 2, unchanged.
- Buttons cloned from the product hero so they match exactly.
- Imagery: QuarkXPress logo and the product-hero model, so slide 1 reads as QuarkXPress at a glance.

**C · Email**
- Blocks: 01 preheader · 02 logo · 03 hero image · 04 headline + intro + primary CTA · 05 three feature rows · 06 audience block + secondary CTA · 07 footer.
- 04 and 06 vary by audience (prospect / subscriber or active maintenance / end-of-life upgrader). Everything else is fixed — that is what makes AI-cloning the variants safe (see DECISIONS: one master email).
- Feature sentences = the product page sentences. Write once in F-01.
- Not yet reconciled with Quark's Pardot templates. Web fonts will fall back in most mail clients: build with Roboto → Arial stack.

## Design calls

Settled 21 Sep — see `DECISIONS.md`: eyebrow row, H1 untouched · three new + three carried-over feature rows · homepage slide uses QuarkXPress imagery.

Still open: "Watch video" button — gone, or one release video? · which three current features survive (Andrew).
