# The O Commons — 3 Design Explorations

Three fully self-contained versions of the site described in `artifacts/o-common.txt`. Each is a single `index.html` (no build step, no framework) sharing one copy of the hero image (`sites/hero.jpg`, the "Inhale/Exhale" performance photo by Rita Kuleva / Aniko Szucs, downsized from the 3024×4032 original to 2000px). All five tabs (About Us, Events, Network, Artworks, Submit Your Questions) are present in every version as smooth-scroll anchor sections with an active-nav indicator; the Impressum line and photo credit appear in every footer.

Open any version by double-clicking its `index.html`. Only external dependencies are two Google Fonts per version; all animation is hand-written CSS/JS (no libraries), all respect `prefers-reduced-motion`.

The photo is a warm, dimly lit vertical stage image (skin/gold tones, bright center, dark bottom edge) — a strong subject with the artist's arms raised. All three versions use it full-bleed under/behind the header, but treat it very differently: warm & archival (V1), red-washed & loud (V2), grayscale & monumental (V3).

---

## Version 1 — `sites/version-1-archival/` — "The Archive"

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

## Version 2 — `sites/version-2-red-ribbon/` — "The Red Ribbon"

**Design style:** Bold activist-poster energy on a near-black canvas: solid red header ribbon, oversized condensed uppercase type, hard edges, high contrast, red-on-black accents. This is the loudest of the three — solidarity as visual volume. Dark mode by default, the only version that is dark-themed throughout the body.

**Image treatment:** Full-viewport (100vh) hero with a duotone treatment: the image is pulled toward grayscale and multiplied with a red wash gradient, fading into near-black at the bottom where the giant headline sits. The photo becomes an atmospheric, protest-poster-like backdrop rather than a documentary photograph. Red ribbon header is fixed and shrinks on scroll.

**Typography:** Archivo (variable width/weight, extra-bold, tightly tracked, all-caps) + Space Grotesk for body. Headline mixes solid, outlined (`-webkit-text-stroke`), and red words for a street-poster rhythm.

**Animations / fancy bits:**
- Infinite red marquee ticker under the hero (mutual-aid slogans).
- Fixed red "ribbon" nav that compresses on scroll.
- Network section as three full-width activist link-rows that slide right and turn red on hover.
- Artworks tiles fill solid red from the bottom on hover (translate-y wipe) with all text inverting to white.
- Vertical "Scroll ↓" cue with a gentle bob animation.
- FAQ accordion (`<details>`) inside the red submit section, answering "Is this legal advice?" etc.

**Inspiration:** Political campaign posters, ACT UP / mutual-aid graphics, Swiss poster design crossed with punk zine energy, Brutalist web design (hard borders, offset grids, no rounded corners).

**Tech/dependencies:** Static HTML + CSS + vanilla JS; Google Fonts (Archivo variable, Space Grotesk).

---

## Version 3 — `sites/version-3-editorial-bauhaus/` — "The Editorial"

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

## How to compare

| | V1 Archival | V2 Red Ribbon | V3 Editorial |
|---|---|---|---|
| Mood | warm, literary, zine-like | loud, activist, urgent | clean, institutional, refined |
| Palette | cream/ink/rubber-stamp red | black/red/white | white/black/red accent |
| Type voice | serif + mono | condensed extra-bold caps | grotesque + neutral body |
| Image treatment | warm, fades into paper | red duotone, darkened | grayscale monument + Ken Burns |
| Dark or light | light | dark | light |
| Signature effect | animated "Fig. 1" bar chart | marquee ticker + red-fill hover tiles | grayscale→color event poster |

All three share the same IA, the same copy (drawn from `o-common.txt`), the same hero credit line, and the same footer Impressum, so differences are purely design-driven and easy to A/B. The "Submit Your Questions" forms are demo-only (they confirm with a button state change; hook up Formspree/Netlify Forms/Google Forms later). The event detail, network links, and artwork entries are all stubs pointing at the right sections, ready for real pages.
