# Matrix Index

Seven 2x2 matrices accompanying *The Synthesis Playbook* (Workshopr facilitation series, Book 6). One foundation matrix from the framework, six recipe matrices.

Each matrix is shipped as both:
- **SVG** — vector, scales infinitely, embeds in browsers, GitHub, book PDFs, slide decks
- **PNG** (optional) — generate with `qlmanage -t -s 1920 -o /tmp <file>.svg` on macOS, or use `rsvg-convert`

## The matrices

### 1. Foundation — Stakes × Politics

Where to leave AI on and where to switch it off, for any engagement.

- **File:** [`stakes-politics-matrix.svg`](stakes-politics-matrix.svg) · [`stakes-politics-matrix.md`](stakes-politics-matrix.md) (ASCII)
- **Source:** Ch. 3 of the book. Native 2x2 in the manuscript.
- **Use when:** Pinning yourself before ANY synthesis. The most-used matrix.

### 2. Discovery — Evidence × Discomfort

Which findings lead the deck, which go in the appendix, which get filed.

- **File:** [`discovery-evidence-discomfort.svg`](discovery-evidence-discomfort.svg)
- **Source:** Ch. 4 of the book — the Step 6 prioritization filter. Derived: the chapter describes both axes in prose; this is the matrix interpretation.
- **Use when:** Step 6 of the Discovery recipe — picking the 3–5 opportunity areas for the deck.

### 3. Strategic Offsite — Decision durability × Political sensitivity

Which decisions go in which artifact: board deck, CEO memo, or confidential appendix.

- **File:** [`offsite-durability-politics.svg`](offsite-durability-politics.svg)
- **Source:** Ch. 5 of the book — Step 3 of the offsite recipe. Derived: the chapter describes the artifact tiering and decision quality scale; this maps them into a 2x2.
- **Use when:** Step 3 of the Offsite recipe — deciding which decisions belong in which artifact.

### 4. Design Sprint — Primary KPI × Secondary constraint

Which of the four possible recommendations (ship / iterate / abandon / third option).

- **File:** [`sprint-speed-defensibility.svg`](sprint-speed-defensibility.svg)
- **Source:** Ch. 6 of the book — Step 4, the four possible recommendations. Derived from the swipe-or-not worked example (speed × audit defensibility). Generalize the axes to your specific hypothesis's conjoined claims.
- **Use when:** Step 4 of the Sprint recipe — picking which of the four recommendations the testing supports.

### 5. Ideation — Dots × Criteria *(native to the book)*

The hot-and-good, hot-but-weak, cool-but-strong, and cool-and-weak shortlist quadrants.

- **File:** [`ideation-dots-criteria.svg`](ideation-dots-criteria.svg)
- **Source:** Ch. 7 of the book — Step 3 (dots-vs-criteria tension surfacer). Native 2x2: the book names three of the four quadrants; the fourth (cool-and-weak = kill list) is implicit.
- **Use when:** Step 3 of the Ideation recipe — finding the off-diagonal cells where the dot vote and the criteria disagree.

### 6. Retro — Dot count × Structural importance

Where the trust sticky lives. Why one-dot stickies can be the most important on the wall.

- **File:** [`retro-dots-importance.svg`](retro-dots-importance.svg)
- **Source:** Ch. 8 of the book — the trust-sticky pattern. Derived: the chapter's worked example demonstrates the bottom-right quadrant; this matrix makes the full picture explicit.
- **Use when:** Step 1–2 of the Retro recipe — triaging stickies after the clusterer and dissent-vs-noise distinguisher.

### 7. Training — Movement × Expectation alignment

Sub-cohort triage. Where the surprising-direction participants and the flags section come from.

- **File:** [`training-movement-expectation.svg`](training-movement-expectation.svg)
- **Source:** Ch. 9 of the book — Step 2 (cohort-pattern surfacer). Derived: the chapter describes both axes in prose; this matrix makes them visible.
- **Use when:** Step 2 of the Training recipe — building the baseline-to-close pairs and finding which participants need named treatment.

---

## Which are native vs. derived

| Matrix | Status | Reasoning |
|---|---|---|
| Stakes × Politics | **Native** | Explicit 2x2 table in Ch. 3 |
| Ideation Dots × Criteria | **Native** | Three of four quadrants named in Ch. 7; fourth is implicit |
| Discovery Evidence × Discomfort | Derived | Both axes described in prose for the Step 6 prioritization; matrix arrangement is a synthesis |
| Offsite Durability × Politics | Derived | Three artifact altitudes + four decision qualities; matrix arrangement maps them cleanly |
| Sprint Speed × Defensibility | Derived | From the swipe-or-not worked example specifically. Generalize the axes per your hypothesis |
| Retro Dots × Importance | Derived | The trust-sticky moment in Ch. 8 demonstrates the bottom-right cell; matrix completes the picture |
| Training Movement × Expectation | Derived | Cohort-pattern surfacer describes both axes; matrix arrangement is interpretation |

The derived matrices are **defensible interpretations** of book material, not invention. If the book and a derived matrix disagree, **the book wins** — open an issue and the matrix will be corrected.

## Visual conventions

All matrices use the same visual language for cross-recipe recognizability:

- **960 × 720 viewBox** (4:3 aspect ratio, fits standard slides)
- **Inter font** with system fallback
- **Axis labels outside the grid** with HIGH/LOW (or named end-states) for tick labels
- **Quadrant color coding by difficulty/importance**:
  - **Green** — the easy cell (obvious call, clean shortlist, file-and-forget)
  - **Yellow** — the judgment cells (off-diagonal, requires human reading)
  - **Red** — the highest-stakes cell (what the synthesis exists to catch)
- **Footer line** restates the book's relevant discipline

## Embedding

In markdown:

```markdown
![](docs/images/stakes-politics-matrix.svg)
```

In InDesign / Affinity Publisher: open the SVG as a placed asset; scales infinitely.

In Keynote / Google Slides: drag the SVG; or convert to PNG first via `qlmanage -t -s 1920 -o /tmp <file>.svg`.

For Substack or blog posts that require raster: PNG via the above command.

## Generating PNG previews

```bash
cd docs/images/
for svg in *.svg; do
  qlmanage -t -s 1920 -o /tmp "$svg"
done
```

PNGs land in `/tmp/<filename>.svg.png`. Move where needed.

## Source

All matrices derived from *The Synthesis Playbook* by Bill Bulman (Workshopr facilitation series, Book 6). The book is the source of truth for axes, framings, and worked examples.
