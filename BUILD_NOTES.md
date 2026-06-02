# Build Notes — Benjamin F. Henwood Academic Website

**Built:** June 2, 2026  
**Source CV:** `Henwood_CV_June_2026_v2.docx`  
**Target directory:** `/data/.openclaw/workspace/projects/benhenwood-site/`

---

## What Was Built

A complete static academic website for Professor Benjamin F. Henwood, modeled after dennisculhane.com in style: clean, minimal, white background, professional typography, USC cardinal accent color.

### Files
```
index.html              — Main site (49 KB, ~1,000+ lines)
assets/css/style.css    — Stylesheet (~300 lines, pure CSS3)
assets/img/headshot.jpg — Headshot (pre-existing, linked via relative path)
BUILD_NOTES.md          — This file
```

---

## Sections

1. **Sticky Navigation** — Top nav bar with USC cardinal underline accent. Responsive collapse on mobile.

2. **Hero / Header** — Name, title (Feldman Professorship), institution, tagline, headshot right-aligned (centered on mobile), quick-link buttons.

3. **About** — Paragraph bio, 4-item stats bar (100+ pubs, $20M+ funding, HPRI Director, Housing First book), quick-link buttons to USC Faculty, Google Scholar, HPRI, email.

4. **Research** — Organized in collapsible `<details>/<summary>` sections (CSS-only, no JavaScript):
   - Books section: Oxford UP *Housing First* + Italian translation (FrancoAngeli)
   - **9 thematic publication categories** (selected representative papers from 100+):
     1. Housing First & Permanent Supportive Housing
     2. Homelessness Count & Methodology
     3. Aging & Homelessness
     4. Mental Health & Recovery
     5. Basic Income & Economic Interventions
     6. COVID-19, Wildfires & Homelessness
     7. Health Services & Integration
     8. Youth, TAY & HIV Risk
     9. Policy Analysis, Commentaries & Invited Articles
   - Policy Briefs & Technical Reports section: PATHS reports (sweeps, wildfires, ICE raids), Basic Income brief, Grants Pass amicus brief, RAND veterans report

5. **Policy & Writing** — Op-eds (The Hill 2020 & forthcoming 2026, Assembly testimony), links to HPRI, The Conversation, Oxford Bibliographies.

6. **Media** — Coverage list: NBC News, LA Times, NPR, The Hill, USC News, RAND. Links to USC faculty profile.

7. **Contact / For Media** — Two-column grid: media inquiry + office address (MRF Suite 224).

8. **Footer** — © 2026, USC link, contact.

---

## Design Decisions

- **Color palette:** White background, `#1a1a1a` body text, `#990000` USC cardinal for links/accents
- **Typography:** Georgia serif for headings, Helvetica Neue/Arial sans for body — same classic academic feel as dennisculhane.com
- **Layout:** `max-width: 860px; margin: 0 auto` centered column
- **Collapsible sections:** Native HTML `<details>`/`<summary>` — zero JavaScript
- **Responsive:** CSS Grid/Flexbox, media queries at 680px and 400px. Mobile: stacked layout, headshot centered on top, 2-column stats grid
- **Print stylesheet:** `@media print` hides nav/footer, shows clean publication list
- **Smooth transitions:** hover states on all links and buttons

---

## Publication Coverage

The CV contains 100+ peer-reviewed articles. For web readability, the site includes approximately **60–70 representative papers** across categories, weighted toward:
- Recent high-impact work (2022–2026)
- Award-winning papers (Slavin-Patti, Editor's Choice, Best Publication awards)
- Seminal/foundational papers (Housing First RCTs, mortality, PIT methodology)
- Cross-cutting themes (PATHS cohort, Miracle Money, CAPABLE, Grants Pass)

Student-mentored papers are noted with ★ asterisk per CV convention.

---

## Known Gaps / Future Enhancements

- **Google Scholar link:** Placeholder URL — confirm Ben's actual Scholar profile ID
- **CV PDF download:** No PDF linked yet; could link to an uploaded CV file
- **DOI links:** Titles currently unlinked; adding DOI URLs per paper would improve discoverability
- **Complete publication list:** ~40 additional papers not shown; consider a separate `/publications.html` with full list
- **Analytics:** No tracking — add if desired
- **Favicon:** Not included; USC favicon or custom could be added

---

## Source Data

Parsed from `Henwood_CV_June_2026_v2.docx` using `python-docx`. Bio text adapted from task spec. Publication details drawn directly from CV paragraphs.
