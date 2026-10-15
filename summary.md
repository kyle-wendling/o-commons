# The O Commons — Immigrant Artists Mutual Aid

**Live site: <https://kyle-wendling.github.io/o-commons/>**

A mutual aid network for immigrant artists **and artists-scholars** on O‑1 visas. The live site is a single self-contained `index.html` (no build step, no framework) served by GitHub Pages from `docs/`.

```
docs/
  index.html                              # the live site (formerly "Version 2 — The Red Ribbon")
  hero.jpg                                # "Inhale/Exhale" performance photo, Rita Kuleva / Aniko Szucs
  legacy/
    index.html                            # archive index describing all three explorations
    version-1-archival/index.html         # archived exploration
    version-3-editorial-bauhaus/index.html # archived exploration
artifacts/
  o-common.txt                            # canonical source copy
  Rita Exhibition.jpg                     # reference photo supplied by the client
```

`artifacts/o-common.txt` is the canonical text. All five tabs — About Us, Events, Network, Artworks, Submit Your Questions — are smooth-scroll anchor sections with an active-nav indicator. The Impressum line appears in the footer. The only external dependency is two Google Fonts (Archivo, Space Grotesk); all animation is hand-written CSS/JS and respects `prefers-reduced-motion`.

The hero is a warm, dimly lit vertical stage photo (skin/gold tones, bright center, dark bottom edge) with the artist's arms raised. On the live site it is treated as a crimson duotone backdrop under the headline.

---

## Revision 2 — applied 2026-10-15

The client's second round of feedback, applied to the live site. Everything below this section describes the site as it now stands; the "Legacy archive" section further down is **superseded v1 material** kept only for reference.

| # | Request | What changed |
|---|---|---|
| 1 | Darker red, closer to crimson/burgundy | `--red` set to `#8C1A2B`; new `--red-bright #E25563` accent. Both contrast-verified against WCAG. |
| 2 | Landing copy | "and artists-scholars" added to the tagline; "Peer knowledge…" moved to its own line; hero photo credit deleted. |
| 3 | Marquee stars + words | `✳` stars recolored to the accent red (brighter than the background red); "Artist-Scholars" and "Scholars" added to both track halves. |
| 4 | About Us | Two columns collapsed to one; three paragraphs — the original long opening paragraph, the "Immigration attorneys…" paragraph, and the "The O Commons fills this gap…" pull-quote. |
| 5 | Events | "Join in person" and "Join online" buttons added, linking to the two Eventbrite URLs for the October 23 launch event. |
| 6 | Network | "and scholars" added; the self-petition note appended; Curatorial Repository description replaced. |
| 7 | Artworks | "04 Paper as Material" replaced by "04 — Archive of Artworks"; reduced to three cards (Archive of Artworks, Immigration Memorabilia, Open Call). |
| 8 | Submit Your Questions | Section index shrunk so "05 — Ask anything" shares the heading line; form rebuilt as an aligned label/input grid with matching underlines. |

Two adjustments beyond the literal list, both needed to make the requests read correctly:

- The Artworks cards were bottom-aligned, which left the three tags at different heights once the third card gained a subtitle. They are now top-aligned.
- The first two Artworks cards duplicated their title as a small label above the heading. Those labels became `01`/`02`/`03` to match the section's numbering.

**Also in this round:** the three-version chooser and the two unselected explorations moved to `docs/legacy/`, and the Red Ribbon version was promoted to `docs/index.html` so it became the live landing page.

**Hero sizing fix (2026-10-15):** the headline was bottom-anchored inside a fixed `height:100vh` hero, so on short viewports — typically wide monitors — the top line slid under the fixed ribbon. The hero is now `min-height:100vh` with top padding, and the headline scales on `min(9vw,15vh)`. Verified clear of the ribbon from 1280×720 through 3440×700.

---

## The live site — "The Red Ribbon"

**Design style:** Bold activist-poster energy on a near-black canvas: a dark crimson ribbon nav, oversized condensed uppercase type, hard edges, high contrast. Dark mode throughout — the loudest of the explorations, solidarity as visual volume.

**Palette:** `--ink #141414`, `--paper #F5F2EC`, `--red #8C1A2B` (dark crimson/burgundy), `--red-bright #E25563` (accent — marquee stars, section labels, and the highlighted word in the hero headline).

**Image treatment:** Full-viewport hero with the image pulled toward grayscale and multiplied with a crimson wash gradient, fading into near-black at the bottom where the giant headline sits. The photo becomes an atmospheric, protest-poster-like backdrop rather than a documentary photograph.

**Typography:** Archivo (variable width/weight, extra-bold, tightly tracked, all-caps) + Space Grotesk for body. The headline mixes solid, outlined (`-webkit-text-stroke`), and crimson words for a street-poster rhythm.

**Animations / fancy bits:**
- Infinite crimson marquee ticker under the hero, its `✳` stars set in the brighter accent red.
- Fixed ribbon nav that compresses on scroll.
- Network section as three full-width link-rows that slide right and turn crimson on hover.
- Artworks tiles fill solid crimson from the bottom on hover (translate-y wipe) with all text inverting to white.
- Vertical "Scroll ↓" cue with a gentle bob animation.
- FAQ accordion (`<details>`) inside the crimson submit section, answering "Is this legal advice?" etc.

**Inspiration:** Political campaign posters, ACT UP / mutual-aid graphics, Swiss poster design crossed with punk zine energy, Brutalist web design (hard borders, offset grids, no rounded corners).

---

## The legacy archive — `docs/legacy/` (superseded v1 material)

> **Note:** everything from here down describes the **v1 exploration round** and is kept for reference only. It is not the live site and is not maintained. The live site is described above.

Two earlier explorations were kept for reference when the Red Ribbon direction was selected. They share the same IA and copy, so the differences are purely design-driven.

| | V1 Archival | V3 Editorial |
|---|---|---|
| Mood | warm, literary, zine-like | clean, institutional, refined |
| Palette | cream/ink/rubber-stamp red | white/black/red accent |
| Type voice | Fraunces serif + IBM Plex Mono | Space Grotesk + Inter |
| Image treatment | warm, fades into paper | grayscale monument + Ken Burns |
| Signature effect | animated "Fig. 1" bar chart | grayscale→color event poster |

V1 is an aged-paper dossier aesthetic — the organization's material is literally paperwork, so the site reads like a beautifully typeset case file. V3 is Swiss-grid editorial: white gallery background, numbered sections, one disciplined red accent, and a cinematic 22s Ken Burns drift on the hero. Both are frozen and not maintained.

---

## Version 1 — `docs/legacy/version-1-archival/` — "The Archive"

**Design style:** Warm archival-document aesthetic. Aged-paper cream (#F2EEE3), typewriter mono labels, hairline rules, a rubber-stamp red (#A83226), and Fraunces (an old-style serif) for everything editorial. The whole site reads like a beautifully typeset dossier or mutual-aid zine — fitting for an organization whose material is literally paperwork: petitions, letters, case files.

**Image treatment:** Full-bleed hero at 82vh with the warm tones preserved (slight desaturation only). A single gradient fades the photo's dark bottom directly into the page's cream background, so the image dissolves into the page rather than ending in a hard line — the "photo pinned at the top of the document" feel. White text sits over the dark upper region for contrast; the photo credit is overlaid bottom-right.

**Typography:** Fraunces (display serif) + IBM Plex Mono (labels, metadata, "Fig. 1" captions).

**Animations / fancy bits:**
- Scroll-reveal (IntersectionObserver) on every block.
- An animated "Fig. 1 — The weight of the process" horizontal bar chart: red bars grow when scrolled into view, with mono annotations — data-as-vignette (illustrative figures, clearly labeled).
- The Artworks cards are slightly rotated like pinned documents and straighten with a hard offset shadow on hover.
- A rotated red "stamp" element on the hero ("Mutual aid · NYC · est. 2026").
- Scroll-spy active nav underlines.

**Inspiration:** Archival design (Chronicling America / library digital collections), museum exhibition catalogs, artist-book design, bureaucratic paperwork itself turned into visual language.

**Tech/dependencies:** Zero-JS-dependency static HTML + CSS + vanilla JS; Google Fonts (Fraunces, IBM Plex Mono). Works offline (fonts just fall back).

---

## Version 3 — `docs/legacy/version-3-editorial-bauhaus/` — "The Editorial"

**Design style:** Swiss/international-typographic-style editorial: white gallery-like background, strict grid, numbered sections (01–05) with rules, giant Space Grotesk headlines with an outlined-word motif, generous whitespace, one disciplined red accent. The most refined and "institution-ready" of the three — the direction I'd pick if the audience includes funders, universities (CUNY), and press.

**Image treatment:** The photo is shown at its strongest: 100vh full-bleed, converted to full grayscale with a bottom ink fade, with a very slow Ken Burns drift (22s scale animation) that makes the opening feel cinematic rather than static. The same image reappears small as the event's "poster," colorized on hover — a deliberate design echo: the launch event re-uses the landing image, inverting the treatment (grayscale → color on hover).

**Typography:** Space Grotesk (headlines, labels, numbers) + Inter (body). Uppercase micro-labels, oversized numerals, tight tracking.

**Animations / fancy bits:**
- Ken Burns slow zoom on the hero.
- Ink ticker strip (black, red bullet separators) between hero and content.
- Event card lifts with a solid red offset shadow on hover while its grayscale poster blooms into color.
- Artworks cards get a hard black offset shadow on hover (print-like).
- Scroll-spy nav underline in red.

**Inspiration:** Swiss/Bauhaus grid design, Kinfolk/Apartment-style editorial layouts, museum biennial websites, Jose Müller-Brockmann posters; the grayscale monumentalism of documentary photo essays.

**Tech/dependencies:** Static HTML + CSS + vanilla JS; Google Fonts (Space Grotesk, Inter).

---

## Adding the site to a host

`docs/` is already the GitHub Pages publish directory, so `docs/index.html` is the live landing page. To preview locally, serve the folder rather than opening the file directly, since the hero path is relative:

```sh
cd docs && python3 -m http.server 8899
```

